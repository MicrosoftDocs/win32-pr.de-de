---
title: Color2-Attribut (Fill) (VML)
description: Color2-Attribut (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339085"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="bdff4-103">Color2-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="bdff4-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="bdff4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="bdff4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bdff4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bdff4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bdff4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="bdff4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bdff4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bdff4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bdff4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bdff4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bdff4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bdff4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bdff4-110">Definiert eine zweite Farbe für Füllungen.</span><span class="sxs-lookup"><span data-stu-id="bdff4-110">Defines a second color for fills.</span></span> <span data-ttu-id="bdff4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bdff4-111">Read/write.</span></span> <span data-ttu-id="bdff4-112">[Vgcolor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="bdff4-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="bdff4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="bdff4-113">**Applies To**</span></span>

[<span data-ttu-id="bdff4-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="bdff4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="bdff4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="bdff4-115">**Tag Syntax**</span></span>

<span data-ttu-id="bdff4-116"><v: *Element* color2 = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="bdff4-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="bdff4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="bdff4-117">**Script Syntax**</span></span>

<span data-ttu-id="bdff4-118">*Element* . color2 = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="bdff4-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="bdff4-119">*Ausdruck* = *Element*. color2</span><span class="sxs-lookup"><span data-stu-id="bdff4-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="bdff4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="bdff4-120">**Remarks**</span></span>

<span data-ttu-id="bdff4-121">Eine zweite Farbe wird verwendet, wenn ein Fülltyp ein Muster oder ein Farbverlauf ist.</span><span class="sxs-lookup"><span data-stu-id="bdff4-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="bdff4-122">Der Standardwert ist **weiß**.</span><span class="sxs-lookup"><span data-stu-id="bdff4-122">The default value is **White**.</span></span>

<span data-ttu-id="bdff4-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="bdff4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bdff4-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bdff4-124">**Example**</span></span>

<span data-ttu-id="bdff4-125">Der Fülltyp der Form ist ein Muster, bei dem die Vordergrundfarbe durch das Quell Bild definiert wird, der transparente Hintergrund jedoch durch die zweite Farbe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bdff4-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 