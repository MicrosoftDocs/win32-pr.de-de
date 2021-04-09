---
title: VML-Fokus Attribut
description: VML-Fokus Attribut
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039585"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="93f7a-103">VML-Fokus Attribut</span><span class="sxs-lookup"><span data-stu-id="93f7a-103">VML Focus Attribute</span></span>

<span data-ttu-id="93f7a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="93f7a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="93f7a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="93f7a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="93f7a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="93f7a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="93f7a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="93f7a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="93f7a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="93f7a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="93f7a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="93f7a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="93f7a-110">Definiert den Mittelpunkt einer linearen Farbverlaufsfüllung.</span><span class="sxs-lookup"><span data-stu-id="93f7a-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="93f7a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="93f7a-111">Read/write.</span></span> <span data-ttu-id="93f7a-112">**Vgbruchteile**.</span><span class="sxs-lookup"><span data-stu-id="93f7a-112">**VgFraction**.</span></span>

<span data-ttu-id="93f7a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="93f7a-113">**Applies To**</span></span>

[<span data-ttu-id="93f7a-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="93f7a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="93f7a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="93f7a-115">**Tag Syntax**</span></span>

<span data-ttu-id="93f7a-116"><v: *Element* Fokus = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="93f7a-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="93f7a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="93f7a-117">**Script Syntax**</span></span>

<span data-ttu-id="93f7a-118">*Element* . Focus = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="93f7a-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="93f7a-119">*Ausdruck* = *Element*. Fokus</span><span class="sxs-lookup"><span data-stu-id="93f7a-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="93f7a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="93f7a-120">**Remarks**</span></span>

<span data-ttu-id="93f7a-121">Definiert die Startposition der Mitte der Mischung.</span><span class="sxs-lookup"><span data-stu-id="93f7a-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="93f7a-122">Die Werte reichen von 100% bis-100%.</span><span class="sxs-lookup"><span data-stu-id="93f7a-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="93f7a-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="93f7a-123">The default value is 0.</span></span> <span data-ttu-id="93f7a-124">Ein Wert von 100% (oder-100%) Verschiebt den Fokus so, dass die Richtung der Blend umkehren wird (sodass die **Farbe** und der **color2** umkehren).</span><span class="sxs-lookup"><span data-stu-id="93f7a-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="93f7a-125">Mit einem Wert von 50% wird die Mischung geändert, sodass sich die **Farbe** an beiden Enden und der **color2** -Wert in der Mitte befindet.</span><span class="sxs-lookup"><span data-stu-id="93f7a-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="93f7a-126">Mit dem Wert-50% wird die Mischung geändert, sodass sich **color2** an beiden Enden und die **Farbe** in der Mitte befindet.</span><span class="sxs-lookup"><span data-stu-id="93f7a-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="93f7a-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="93f7a-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="93f7a-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="93f7a-128">**Example**</span></span>

<span data-ttu-id="93f7a-129">Der Farbverlaufs Fokus der Füllung wird so verschoben, dass Rot (**Farbe**) ein Band in der Mitte der Form ist und dass der obere und untere Rand blau (**color2**) sind.</span><span class="sxs-lookup"><span data-stu-id="93f7a-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 