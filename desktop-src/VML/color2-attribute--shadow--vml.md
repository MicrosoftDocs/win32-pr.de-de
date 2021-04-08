---
title: Color2-Attribut (Schatten) (VML)
description: Color2-Attribut (Schatten) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729193"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="0d253-103">Color2-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="0d253-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="0d253-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0d253-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0d253-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0d253-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0d253-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0d253-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0d253-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0d253-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0d253-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0d253-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0d253-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0d253-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0d253-110">Definiert die zweite Farbe eines Schattens.</span><span class="sxs-lookup"><span data-stu-id="0d253-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="0d253-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0d253-111">Read/write.</span></span> <span data-ttu-id="0d253-112">**Vgcolor**.</span><span class="sxs-lookup"><span data-stu-id="0d253-112">**VgColor**.</span></span>

<span data-ttu-id="0d253-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0d253-113">**Applies To**</span></span>

[<span data-ttu-id="0d253-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="0d253-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="0d253-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0d253-115">**Tag Syntax**</span></span>

<span data-ttu-id="0d253-116"><v: *Element* color2 = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="0d253-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="0d253-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="0d253-117">**Script Syntax**</span></span>

<span data-ttu-id="0d253-118">*Element* . color2 = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0d253-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="0d253-119">*Ausdruck* = *Element*. color2</span><span class="sxs-lookup"><span data-stu-id="0d253-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="0d253-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0d253-120">**Remarks**</span></span>

<span data-ttu-id="0d253-121">Verwenden Sie eine zweite Farbe, um besondere Schatteneffekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d253-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="0d253-122">Weitere Informationen zu zweiten Farben finden Sie unter dem [Type](type-attribute--shadow--vml.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="0d253-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="0d253-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0d253-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0d253-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0d253-124">**Example**</span></span>

<span data-ttu-id="0d253-125">Der Schatten ist für eine zweite Farbe blau.</span><span class="sxs-lookup"><span data-stu-id="0d253-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 