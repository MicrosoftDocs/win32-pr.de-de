---
title: VML-Attribut "gewinnen"
description: VML-Attribut "gewinnen"
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390671"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="a29c5-103">VML-Attribut "gewinnen"</span><span class="sxs-lookup"><span data-stu-id="a29c5-103">VML Gain Attribute</span></span>

<span data-ttu-id="a29c5-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a29c5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a29c5-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a29c5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a29c5-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a29c5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a29c5-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a29c5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a29c5-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a29c5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a29c5-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a29c5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a29c5-110">Definiert die Intensität aller Farben in einem Bild.</span><span class="sxs-lookup"><span data-stu-id="a29c5-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="a29c5-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a29c5-111">Read/write.</span></span> <span data-ttu-id="a29c5-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="a29c5-112">**VgNumber**.</span></span>

<span data-ttu-id="a29c5-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a29c5-113">**Applies To**</span></span>

[<span data-ttu-id="a29c5-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a29c5-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a29c5-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a29c5-115">**Tag Syntax**</span></span>

<span data-ttu-id="a29c5-116"><v: *Element* Gewinn = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="a29c5-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="a29c5-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a29c5-117">**Script Syntax**</span></span>

<span data-ttu-id="a29c5-118">*Element* . Gewinn = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a29c5-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="a29c5-119">*Ausdruck* = *Element*. Gewinn</span><span class="sxs-lookup"><span data-stu-id="a29c5-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="a29c5-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a29c5-120">**Remarks**</span></span>

<span data-ttu-id="a29c5-121">Dieses Attribut definiert, wie hell die Farbe weiß ist, was sich auf alle anderen Farben auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a29c5-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="a29c5-122">Die Werte reichen von 0 bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="a29c5-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="a29c5-123">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="a29c5-123">The default value is 1.0.</span></span> <span data-ttu-id="a29c5-124">Der Wert 0 zeigt kein Bild an.</span><span class="sxs-lookup"><span data-stu-id="a29c5-124">A value of 0 displays no image.</span></span> <span data-ttu-id="a29c5-125">Werte, die größer als 1 sind, erleichtern das Bild, und Werte kleiner als 1 machen das Bild grau.</span><span class="sxs-lookup"><span data-stu-id="a29c5-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="a29c5-126">Dieses Attribut kann verwendet werden, um interessante Effekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a29c5-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="a29c5-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a29c5-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="a29c5-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a29c5-128">**Example**</span></span>

<span data-ttu-id="a29c5-129">Das Bild wird mit allen Farben angezeigt, die in der grau Richtung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a29c5-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 