---
title: Rotation-Attribut (Form) (VML)
description: Rotation-Attribut (Form) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039556"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="c1c42-103">Rotation-Attribut (Form) (VML)</span><span class="sxs-lookup"><span data-stu-id="c1c42-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="c1c42-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c1c42-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c1c42-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c1c42-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c1c42-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c1c42-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c1c42-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c1c42-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c1c42-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c1c42-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c1c42-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c1c42-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c1c42-110">Definiert den Winkel, in dem eine Form gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="c1c42-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="c1c42-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c1c42-111">Read/write.</span></span> <span data-ttu-id="c1c42-112">[Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c1c42-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="c1c42-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c1c42-113">**Applies To**</span></span>

[<span data-ttu-id="c1c42-114">Form</span><span class="sxs-lookup"><span data-stu-id="c1c42-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c1c42-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c1c42-115">**Tag Syntax**</span></span>

<span data-ttu-id="c1c42-116"><v: *Element* Style = "Rotation: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c1c42-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="c1c42-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c1c42-117">**Script Syntax**</span></span>

<span data-ttu-id="c1c42-118">*Element* . Rotation = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c1c42-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="c1c42-119">*Ausdruck* = *Element*. Drehung</span><span class="sxs-lookup"><span data-stu-id="c1c42-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="c1c42-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c1c42-120">**Remarks**</span></span>

<span data-ttu-id="c1c42-121">Der Wert in Grad kann positiv oder negativ sein, und Werte, die größer als 360 sind, werden auf einen 360-Grad-Kreis modularisiert.</span><span class="sxs-lookup"><span data-stu-id="c1c42-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="c1c42-122">Positive Winkel sind im Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="c1c42-122">Positive angles are clockwise.</span></span> <span data-ttu-id="c1c42-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="c1c42-123">The default value is 0.</span></span>

<span data-ttu-id="c1c42-124">Beachten Sie, dass die Form nach der Drehung neu positioniert wird, um die neuen Begrenzungsfeld Koordinaten widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="c1c42-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="c1c42-125">Beachten Sie außerdem, dass für die Skripterstellung das **Format Attribut nicht** verwendet wird und dass die **Drehung** als direktes Attribut der Form behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="c1c42-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="c1c42-126">Das **Rotations** Attribut ähnelt dem Standard-HTML- **Rotations** Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="c1c42-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="c1c42-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c1c42-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="c1c42-128">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="c1c42-128">**See Also**</span></span>

<span data-ttu-id="c1c42-129">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c1c42-129">**Example**</span></span>

<span data-ttu-id="c1c42-130">Das Rechteck wird um 45 Grad gekippt.</span><span class="sxs-lookup"><span data-stu-id="c1c42-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="c1c42-131">[Beispiel für das Rotations Attribut](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1c42-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="c1c42-132">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="c1c42-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 