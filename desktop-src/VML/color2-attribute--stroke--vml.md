---
title: Color2-Attribut (Strich) (VML)
description: Color2-Attribut (Strich) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473764"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="0e7b0-103">Color2-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="0e7b0-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="0e7b0-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0e7b0-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0e7b0-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0e7b0-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0e7b0-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0e7b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0e7b0-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0e7b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0e7b0-110">Definiert eine zweite Farbe für Striche.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-110">Defines a second color for strokes.</span></span> <span data-ttu-id="0e7b0-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-111">Read/write.</span></span> <span data-ttu-id="0e7b0-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-112">**String**.</span></span>

<span data-ttu-id="0e7b0-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0e7b0-113">**Applies To**</span></span>

[<span data-ttu-id="0e7b0-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="0e7b0-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0e7b0-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0e7b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="0e7b0-116"><v: *Element* color2 = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="0e7b0-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="0e7b0-117">Skript Syntax</span><span class="sxs-lookup"><span data-stu-id="0e7b0-117">Script Syntax</span></span>

<span data-ttu-id="0e7b0-118">*Element* . color2 = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0e7b0-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="0e7b0-119">*Ausdruck* = *Element*. color2</span><span class="sxs-lookup"><span data-stu-id="0e7b0-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="0e7b0-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0e7b0-120">**Remarks**</span></span>

<span data-ttu-id="0e7b0-121">Eine zweite Farbe wird verwendet, wenn der Fülltyp eines Strichs ein Muster ist.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="0e7b0-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0e7b0-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="0e7b0-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0e7b0-123">**Example**</span></span>

<span data-ttu-id="0e7b0-124">Der Strich der Form ist eine Musterfüllung, bei der die Füllung durch das Quell Bild definiert wird, der transparente Hintergrund jedoch durch die zweite Farbe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0e7b0-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 