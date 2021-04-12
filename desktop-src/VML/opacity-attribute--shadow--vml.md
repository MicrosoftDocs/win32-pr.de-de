---
title: Opacity-Attribut (Schatten) (VML)
description: Opacity-Attribut (Schatten) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390449"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="724af-103">Opacity-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="724af-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="724af-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="724af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="724af-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="724af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="724af-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="724af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="724af-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="724af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="724af-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="724af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="724af-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="724af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="724af-110">Bestimmt die Transparenz eines Schattens.</span><span class="sxs-lookup"><span data-stu-id="724af-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="724af-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="724af-111">Read/write.</span></span> <span data-ttu-id="724af-112">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="724af-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="724af-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="724af-113">**Applies To**</span></span>

[<span data-ttu-id="724af-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="724af-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="724af-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="724af-115">**Tag Syntax**</span></span>

<span data-ttu-id="724af-116"><v: *Element* Deckkraft = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="724af-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="724af-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="724af-117">**Script Syntax**</span></span>

<span data-ttu-id="724af-118">*Element* . Opacity = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="724af-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="724af-119">*Ausdruck* = *Element*. Deckkraft</span><span class="sxs-lookup"><span data-stu-id="724af-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="724af-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="724af-120">**Remarks**</span></span>

<span data-ttu-id="724af-121">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="724af-121">The default value is 1.</span></span> <span data-ttu-id="724af-122">Der Wert 0 (null) führt zu einem vollständig transparenten Schatten.</span><span class="sxs-lookup"><span data-stu-id="724af-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="724af-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="724af-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="724af-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="724af-124">**Example**</span></span>

<span data-ttu-id="724af-125">Die Form hat einen Schatten, der 50% transparent ist.</span><span class="sxs-lookup"><span data-stu-id="724af-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 