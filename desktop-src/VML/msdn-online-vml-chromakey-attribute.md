---
title: VML Chromakey-Attribut
description: VML Chromakey-Attribut
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315633"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="605d0-103">VML Chromakey-Attribut</span><span class="sxs-lookup"><span data-stu-id="605d0-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="605d0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="605d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="605d0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="605d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="605d0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="605d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="605d0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="605d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="605d0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="605d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="605d0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="605d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="605d0-110">Definiert den Farbwert des Bilds, das als transparent behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="605d0-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="605d0-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="605d0-111">Read/write.</span></span> <span data-ttu-id="605d0-112">**Vgcolor**.</span><span class="sxs-lookup"><span data-stu-id="605d0-112">**VgColor**.</span></span>

<span data-ttu-id="605d0-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="605d0-113">**Applies To**</span></span>

[<span data-ttu-id="605d0-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="605d0-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="605d0-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="605d0-115">**Tag Syntax**</span></span>

<span data-ttu-id="605d0-116"><v: *Element* Chromakey = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="605d0-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="605d0-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="605d0-117">**Script Syntax**</span></span>

<span data-ttu-id="605d0-118">*Element* . Chromakey = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="605d0-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="605d0-119">*Ausdruck* = *Element*. Chromakey</span><span class="sxs-lookup"><span data-stu-id="605d0-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="605d0-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="605d0-120">**Remarks**</span></span>

<span data-ttu-id="605d0-121">Verwenden Sie dieses Attribut, um Teile eines Bilds transparent zu machen, indem Sie die Transparenz an eine bestimmte Farbe anschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="605d0-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="605d0-122">Wenn Sie z. b. den **Chromakey** -Wert **schwarz** machen, ist jeder Teil des Bilds, der schwarz ist, transparent, und die Füllfarbe wird in diesem Teil des Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="605d0-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="605d0-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="605d0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="605d0-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="605d0-124">**Example**</span></span>

<span data-ttu-id="605d0-125">Die Bereiche des Bilds, die solide schwarz sind, werden transparent, sodass die grüne Füllfarbe stattdessen durch diese Bereiche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="605d0-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 