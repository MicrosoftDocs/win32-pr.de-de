---
title: VML-Metal-Attribut
description: VML-Metal-Attribut
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390356"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="32c61-103">VML-Metal-Attribut</span><span class="sxs-lookup"><span data-stu-id="32c61-103">VML Metal Attribute</span></span>

<span data-ttu-id="32c61-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="32c61-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32c61-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="32c61-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32c61-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="32c61-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32c61-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="32c61-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32c61-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="32c61-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32c61-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="32c61-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32c61-110">Bestimmt, ob die Oberfläche der extrudierten Form Metal ähnelt.</span><span class="sxs-lookup"><span data-stu-id="32c61-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="32c61-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="32c61-111">Read/write.</span></span> <span data-ttu-id="32c61-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="32c61-112">**VgTriState**.</span></span>

<span data-ttu-id="32c61-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="32c61-113">**Applies To**</span></span>

[<span data-ttu-id="32c61-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="32c61-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="32c61-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="32c61-115">**Tag Syntax**</span></span>

<span data-ttu-id="32c61-116"><o: *Element* Metal = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="32c61-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="32c61-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="32c61-117">**Script Syntax**</span></span>

<span data-ttu-id="32c61-118">*Element* . Metal = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="32c61-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="32c61-119">*Ausdruck* = *Element*. Metal</span><span class="sxs-lookup"><span data-stu-id="32c61-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="32c61-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="32c61-120">**Remarks**</span></span>

<span data-ttu-id="32c61-121">Wenn diese Eigenschaft auf " **true**" festgelegt ist, bewirkt dieses Attribut, dass das für die Legende reflektierte Licht die Material Farbe anstelle der hellen Quellfarbe ist, sodass das Objekt mehr Metallic erscheint. Zur weiteren Näherung eines metallischen Materials ist es erforderlich, dass die Spekulation relativ hoch (etwa 1,2) und diffusity relativ niedrig (etwa 0,6) ist.</span><span class="sxs-lookup"><span data-stu-id="32c61-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="32c61-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="32c61-122">The default value is **False**.</span></span>

<span data-ttu-id="32c61-123">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="32c61-123">*Microsoft Office Extensions Attribute*</span></span>

 

 