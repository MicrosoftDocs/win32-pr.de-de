---
title: Size-Attribut (Fill) (VML)
description: Size-Attribut (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948804"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="f041e-103">Size-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="f041e-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="f041e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="f041e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f041e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f041e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f041e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="f041e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f041e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f041e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f041e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f041e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f041e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f041e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f041e-110">Definiert die Größe des Bilds für die Füllung.</span><span class="sxs-lookup"><span data-stu-id="f041e-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="f041e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f041e-111">Read/write.</span></span> <span data-ttu-id="f041e-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="f041e-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="f041e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="f041e-113">**Applies To**</span></span>

[<span data-ttu-id="f041e-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="f041e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="f041e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="f041e-115">**Tag Syntax**</span></span>

<span data-ttu-id="f041e-116"><v: *Element* size = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f041e-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="f041e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="f041e-117">**Script Syntax**</span></span>

<span data-ttu-id="f041e-118">*Element* . Size = "*Ausdruck \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="f041e-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="f041e-119">*Ausdruck* = *Element*. Size</span><span class="sxs-lookup"><span data-stu-id="f041e-119">*expression*=*element*.size</span></span>

<span data-ttu-id="f041e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="f041e-120">**Remarks**</span></span>

<span data-ttu-id="f041e-121">Der Standardwert ist die Größe des ursprünglichen Bilds.</span><span class="sxs-lookup"><span data-stu-id="f041e-121">The default is the size of the original image.</span></span> <span data-ttu-id="f041e-122">Größen, die größer als der shapewert sind, zeigen eine vergrößerte, aber abgeschnittene Version des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="f041e-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="f041e-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="f041e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f041e-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f041e-124">**Example**</span></span>

<span data-ttu-id="f041e-125">Obwohl die ursprüngliche Größe des Bilds 50-bis-50 Punkte beträgt, wird das Bild als 10-bis-10-Bild in der Mitte der Füllung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f041e-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 