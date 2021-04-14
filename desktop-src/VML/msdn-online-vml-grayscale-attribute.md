---
title: VML-Grayscale-Attribut
description: VML-Grayscale-Attribut
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390529"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="8e03e-103">VML-Grayscale-Attribut</span><span class="sxs-lookup"><span data-stu-id="8e03e-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="8e03e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="8e03e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e03e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="8e03e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e03e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="8e03e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e03e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8e03e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e03e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e03e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e03e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e03e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e03e-110">Bestimmt, ob ein Bild im Graustufen Modus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8e03e-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="8e03e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8e03e-111">Read/write.</span></span> <span data-ttu-id="8e03e-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="8e03e-112">**VgTriState**.</span></span>

<span data-ttu-id="8e03e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="8e03e-113">**Applies To**</span></span>

[<span data-ttu-id="8e03e-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="8e03e-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="8e03e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="8e03e-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e03e-116"><v: *Element* Grayscale = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="8e03e-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="8e03e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="8e03e-117">**Script Syntax**</span></span>

<span data-ttu-id="8e03e-118">*Element* . Grayscale = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="8e03e-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="8e03e-119">*Ausdruck* = *Element*. Grayscale</span><span class="sxs-lookup"><span data-stu-id="8e03e-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="8e03e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8e03e-120">**Remarks**</span></span>

<span data-ttu-id="8e03e-121">Wenn der Wert **true** ist, wird das Bild in Graustufen anstelle der Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e03e-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="8e03e-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="8e03e-122">The default is **False**.</span></span>

<span data-ttu-id="8e03e-123">Der Wert basiert auf der CCIR-Empfehlung 709, die eine höhere grüne Gewichtung begünstigt und detailliertere Ergebnisse für die natürliche Farbe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="8e03e-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="8e03e-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="8e03e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="8e03e-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="8e03e-125">**Example**</span></span>

<span data-ttu-id="8e03e-126">Das Bild wird in Graustufen anstelle der Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e03e-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 