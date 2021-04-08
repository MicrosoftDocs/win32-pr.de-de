---
title: Origin-Attribut (Schatten) (VML)
description: Origin-Attribut (Schatten) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729993"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="84a88-103">Origin-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="84a88-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="84a88-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="84a88-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="84a88-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="84a88-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="84a88-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="84a88-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="84a88-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="84a88-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="84a88-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="84a88-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="84a88-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="84a88-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="84a88-110">Definiert den Mittelpunkt des Schattens.</span><span class="sxs-lookup"><span data-stu-id="84a88-110">Defines the center of the shadow.</span></span> <span data-ttu-id="84a88-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="84a88-111">Read/write.</span></span> <span data-ttu-id="84a88-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="84a88-112">**VgVector2D**.</span></span>

<span data-ttu-id="84a88-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="84a88-113">**Applies To**</span></span>

[<span data-ttu-id="84a88-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="84a88-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="84a88-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="84a88-115">**Tag Syntax**</span></span>

<span data-ttu-id="84a88-116"><v: *Element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="84a88-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="84a88-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="84a88-117">**Script Syntax**</span></span>

<span data-ttu-id="84a88-118">*Element* . Origin = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="84a88-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="84a88-119">*Ausdruck* = *Element*. Origin</span><span class="sxs-lookup"><span data-stu-id="84a88-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="84a88-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="84a88-120">**Remarks**</span></span>

<span data-ttu-id="84a88-121">Ein paar von Dezimalstellen Werten der Form, von 50% bis-50%.</span><span class="sxs-lookup"><span data-stu-id="84a88-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="84a88-122">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="84a88-122">The default value is 0,0.</span></span>

<span data-ttu-id="84a88-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="84a88-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="84a88-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="84a88-124">**Example**</span></span>

<span data-ttu-id="84a88-125">Der Schatten weist einen Ursprung auf, der 20% nach unten und 20% rechts vom Ursprung der Form ist.</span><span class="sxs-lookup"><span data-stu-id="84a88-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 