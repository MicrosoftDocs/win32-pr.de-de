---
title: VML ColorMode-Attribut
description: VML ColorMode-Attribut
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390533"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="27b74-103">VML ColorMode-Attribut</span><span class="sxs-lookup"><span data-stu-id="27b74-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="27b74-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="27b74-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="27b74-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="27b74-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="27b74-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="27b74-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="27b74-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="27b74-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="27b74-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="27b74-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="27b74-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="27b74-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="27b74-110">Bestimmt den Modus der Extrusionfarbe.</span><span class="sxs-lookup"><span data-stu-id="27b74-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="27b74-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="27b74-111">Read/write.</span></span> <span data-ttu-id="27b74-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="27b74-112">**VgTriState**.</span></span>

<span data-ttu-id="27b74-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="27b74-113">**Applies To**</span></span>

[<span data-ttu-id="27b74-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="27b74-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="27b74-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="27b74-115">**Tag Syntax**</span></span>

<span data-ttu-id="27b74-116"><o: *Element* ColorMode = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="27b74-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="27b74-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="27b74-117">**Script Syntax**</span></span>

<span data-ttu-id="27b74-118">*Element* . ColorMode = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="27b74-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="27b74-119">*Ausdruck* = *Element*. ColorMode</span><span class="sxs-lookup"><span data-stu-id="27b74-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="27b74-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="27b74-120">**Remarks**</span></span>

<span data-ttu-id="27b74-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="27b74-121">Values include:</span></span>



| <span data-ttu-id="27b74-122">Wert</span><span class="sxs-lookup"><span data-stu-id="27b74-122">Value</span></span>  | <span data-ttu-id="27b74-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27b74-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b74-124">auto</span><span class="sxs-lookup"><span data-stu-id="27b74-124">auto</span></span>   | <span data-ttu-id="27b74-125">Gibt an, dass die Farbe der-Extrusion mit der Füllfarbe der Form übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="27b74-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="27b74-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="27b74-126">Default.</span></span>                |
| <span data-ttu-id="27b74-127">custom</span><span class="sxs-lookup"><span data-stu-id="27b74-127">custom</span></span> | <span data-ttu-id="27b74-128">Gibt an, dass die-Extrusion die Farbe des [Color](color-attribute--extrusion--vml.md) -Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="27b74-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="27b74-129">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="27b74-129">*Microsoft Office Extensions Attribute*</span></span>

 

 