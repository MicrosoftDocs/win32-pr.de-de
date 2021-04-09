---
title: VML focussize-Attribut
description: VML focussize-Attribut
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039583"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="52aa3-103">VML focussize-Attribut</span><span class="sxs-lookup"><span data-stu-id="52aa3-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="52aa3-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="52aa3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="52aa3-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="52aa3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="52aa3-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="52aa3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="52aa3-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="52aa3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="52aa3-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="52aa3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="52aa3-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="52aa3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="52aa3-110">Definiert die Fokus Größe für radiale Füllungen.</span><span class="sxs-lookup"><span data-stu-id="52aa3-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="52aa3-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="52aa3-111">Read/write.</span></span> <span data-ttu-id="52aa3-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="52aa3-112">**VgVector2D**.</span></span>

<span data-ttu-id="52aa3-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="52aa3-113">**Applies To**</span></span>

[<span data-ttu-id="52aa3-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="52aa3-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="52aa3-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="52aa3-115">**Tag Syntax**</span></span>

<span data-ttu-id="52aa3-116"><v: *Element* focussize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="52aa3-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="52aa3-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="52aa3-117">**Script Syntax**</span></span>

<span data-ttu-id="52aa3-118">*Element* . focussize = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="52aa3-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="52aa3-119">*Ausdruck* = *Element*. focussize</span><span class="sxs-lookup"><span data-stu-id="52aa3-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="52aa3-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="52aa3-120">**Remarks**</span></span>

<span data-ttu-id="52aa3-121">Die Werte sind Bruchteile der Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="52aa3-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="52aa3-122">Der erste Wert ist ein Prozentsatz der Füllung am rechten Rand der Form, und der zweite Wert ist ein Prozentsatz der Füllung bis zum unteren Rand der Form.</span><span class="sxs-lookup"><span data-stu-id="52aa3-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="52aa3-123">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="52aa3-123">The default value is 0,0.</span></span> <span data-ttu-id="52aa3-124">Ein **focussize** -Wert von 100%, 100% und eine **focusposition** von 0 (null) würde dazu führen, dass color2 die Mischung vollständig beherrschen würde.</span><span class="sxs-lookup"><span data-stu-id="52aa3-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="52aa3-125">Für ausgeglichene Mischungen werden kleine Werte von ca. 10%, 10% empfohlen.</span><span class="sxs-lookup"><span data-stu-id="52aa3-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="52aa3-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="52aa3-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="52aa3-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="52aa3-127">**Example**</span></span>

<span data-ttu-id="52aa3-128">Die radiale Füllung erstellt eine Mischung, die in der Mitte als blau beginnt und an allen vier Rändern rot wird.</span><span class="sxs-lookup"><span data-stu-id="52aa3-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="52aa3-129">Der Mittelpunkt der Blend wird durch **focusposition** definiert, und die Größe der inneren anfangs Farbe wird durch **focussize** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="52aa3-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 