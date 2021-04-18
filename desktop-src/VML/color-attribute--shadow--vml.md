---
title: Color-Attribut (Schatten) (VML)
description: Color-Attribut (Schatten) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339071"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="a66c4-103">Color-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="a66c4-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="a66c4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a66c4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a66c4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a66c4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a66c4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a66c4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a66c4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a66c4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a66c4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a66c4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a66c4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a66c4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a66c4-110">Definiert die Farbe des Schattens.</span><span class="sxs-lookup"><span data-stu-id="a66c4-110">Defines the color of the shadow.</span></span> <span data-ttu-id="a66c4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a66c4-111">Read/write.</span></span> <span data-ttu-id="a66c4-112">**Vgcolor**.</span><span class="sxs-lookup"><span data-stu-id="a66c4-112">**VgColor**.</span></span>

<span data-ttu-id="a66c4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a66c4-113">**Applies To**</span></span>

[<span data-ttu-id="a66c4-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="a66c4-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="a66c4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a66c4-115">**Tag Syntax**</span></span>

<span data-ttu-id="a66c4-116"><v: *Element* Color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a66c4-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="a66c4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a66c4-117">**Script Syntax**</span></span>

<span data-ttu-id="a66c4-118">*Element* . Color = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a66c4-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="a66c4-119">*Ausdruck* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="a66c4-119">*expression*=*element*.color</span></span>

<span data-ttu-id="a66c4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a66c4-120">**Remarks**</span></span>

<span data-ttu-id="a66c4-121">Verwenden Sie das Color-Attribut, um die Farbe eines Schattens festzulegen oder zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a66c4-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="a66c4-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a66c4-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="a66c4-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a66c4-123">**Example**</span></span>

<span data-ttu-id="a66c4-124">Der Schatten ist grün.</span><span class="sxs-lookup"><span data-stu-id="a66c4-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 