---
title: VML-Attribut "Blacklevel"
description: VML-Attribut "Blacklevel"
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039201"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="33735-103">VML-Attribut "Blacklevel"</span><span class="sxs-lookup"><span data-stu-id="33735-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="33735-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="33735-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="33735-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="33735-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="33735-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="33735-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="33735-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="33735-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="33735-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="33735-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="33735-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="33735-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="33735-110">Definiert die Intensität von schwarz in einem Bild.</span><span class="sxs-lookup"><span data-stu-id="33735-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="33735-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="33735-111">Read/write.</span></span> <span data-ttu-id="33735-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="33735-112">**VgNumber**.</span></span>

<span data-ttu-id="33735-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="33735-113">**Applies To**</span></span>

[<span data-ttu-id="33735-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="33735-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="33735-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="33735-115">**Tag Syntax**</span></span>

<span data-ttu-id="33735-116"><v: *Element* Blacklevel = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="33735-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="33735-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="33735-117">**Script Syntax**</span></span>

<span data-ttu-id="33735-118">*Element* . Blacklevel = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="33735-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="33735-119">*Ausdruck* = *Element*. Blacklevel</span><span class="sxs-lookup"><span data-stu-id="33735-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="33735-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="33735-120">**Remarks**</span></span>

<span data-ttu-id="33735-121">Ermöglicht das Ändern der Farb Ebene, sodass schwarze als echte schwarze angezeigt werden und alle anderen Farben als Schattierungen über schwarz sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="33735-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="33735-122">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="33735-122">The default value is 0.</span></span> <span data-ttu-id="33735-123">Obwohl eine beliebige Zahl zwischen positivem und negativem unendlich zulässig ist, werden Werte kleiner als-0,5 als "alle schwarz" angezeigt, und Werte größer als 0,5 werden als "weiß" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33735-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="33735-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="33735-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="33735-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="33735-125">**Example**</span></span>

<span data-ttu-id="33735-126">Das Bild wird mit sehr dunklen Tönen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33735-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 