---
title: Angle-Attribut (Fill) (VML)
description: Angle-Attribut (Fill) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039518"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="d267b-103">Angle-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="d267b-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="d267b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d267b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d267b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d267b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d267b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d267b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d267b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d267b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d267b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d267b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d267b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d267b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d267b-110">Definiert den Winkel einer Farbverlaufsfüllung.</span><span class="sxs-lookup"><span data-stu-id="d267b-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="d267b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d267b-111">Read/write.</span></span> <span data-ttu-id="d267b-112">[Vgangle](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d267b-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="d267b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="d267b-113">**Applies To**</span></span>

[<span data-ttu-id="d267b-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="d267b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="d267b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="d267b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d267b-116"><v: *Element* Winkel = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="d267b-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="d267b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="d267b-117">**Script Syntax**</span></span>

<span data-ttu-id="d267b-118">*Element* . Angle = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="d267b-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="d267b-119">*Ausdruck* = *Element*. Angle</span><span class="sxs-lookup"><span data-stu-id="d267b-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="d267b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="d267b-120">**Remarks**</span></span>

<span data-ttu-id="d267b-121">Der Vektor eines Farbverlaufs ist senkrecht zum Vektor der Blend-Richtung von einer Farbe zu einer anderen.</span><span class="sxs-lookup"><span data-stu-id="d267b-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="d267b-122">Der Standardwert ist 0 (null) Grad, bei dem es sich um einen horizontalen Vektor von links nach rechts handelt.</span><span class="sxs-lookup"><span data-stu-id="d267b-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="d267b-123">Positive Winkel drehen den Farbverlauf gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="d267b-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="d267b-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="d267b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d267b-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="d267b-125">**Example**</span></span>

<span data-ttu-id="d267b-126">Die Füllung der Form besteht aus einem Farbverlauf von zwei Farben und wird von blau zu rot mit einem Winkel von 45 Grad ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d267b-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="d267b-127">Rot wird in der oberen linken Ecke angezeigt, und blau befindet sich in der unteren rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="d267b-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 