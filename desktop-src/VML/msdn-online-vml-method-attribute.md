---
title: VML-Methoden Attribut
description: VML-Methoden Attribut
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339896"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="90e8b-103">VML-Methoden Attribut</span><span class="sxs-lookup"><span data-stu-id="90e8b-103">VML Method Attribute</span></span>

<span data-ttu-id="90e8b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="90e8b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="90e8b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="90e8b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="90e8b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="90e8b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="90e8b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="90e8b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="90e8b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="90e8b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="90e8b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="90e8b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="90e8b-110">Definiert die Methode, die zum Generieren einer Farbverlaufsfüllung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90e8b-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="90e8b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="90e8b-111">Read/write.</span></span> <span data-ttu-id="90e8b-112">**Vgsigmatype**.</span><span class="sxs-lookup"><span data-stu-id="90e8b-112">**VgSigmaType**.</span></span>

<span data-ttu-id="90e8b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="90e8b-113">**Applies To**</span></span>

[<span data-ttu-id="90e8b-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="90e8b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="90e8b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="90e8b-115">**Tag Syntax**</span></span>

<span data-ttu-id="90e8b-116"><v: *Element* Method = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="90e8b-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="90e8b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="90e8b-117">**Script Syntax**</span></span>

<span data-ttu-id="90e8b-118">*Element* . Method = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="90e8b-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="90e8b-119">*Ausdruck* = *Element*. Method</span><span class="sxs-lookup"><span data-stu-id="90e8b-119">*expression*=*element*.method</span></span>

<span data-ttu-id="90e8b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="90e8b-120">**Remarks**</span></span>

<span data-ttu-id="90e8b-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="90e8b-121">Values include:</span></span>



| <span data-ttu-id="90e8b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="90e8b-122">Value</span></span>  | <span data-ttu-id="90e8b-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90e8b-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="90e8b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="90e8b-124">None</span></span>   | <span data-ttu-id="90e8b-125">Keine Sigma-Füllung.</span><span class="sxs-lookup"><span data-stu-id="90e8b-125">No sigma fill.</span></span>       |
| <span data-ttu-id="90e8b-126">Linear</span><span class="sxs-lookup"><span data-stu-id="90e8b-126">Linear</span></span> | <span data-ttu-id="90e8b-127">Lineare Sigma-Füllung.</span><span class="sxs-lookup"><span data-stu-id="90e8b-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="90e8b-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="90e8b-128">Sigma</span></span>  | <span data-ttu-id="90e8b-129">Sigma-Füllung.</span><span class="sxs-lookup"><span data-stu-id="90e8b-129">Sigma fill.</span></span> <span data-ttu-id="90e8b-130">Standard.</span><span class="sxs-lookup"><span data-stu-id="90e8b-130">Default.</span></span> |
| <span data-ttu-id="90e8b-131">Any</span><span class="sxs-lookup"><span data-stu-id="90e8b-131">Any</span></span>    | <span data-ttu-id="90e8b-132">Eine beliebige Sigma-Füllung.</span><span class="sxs-lookup"><span data-stu-id="90e8b-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="90e8b-133">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="90e8b-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="90e8b-134">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="90e8b-134">**Example**</span></span>

<span data-ttu-id="90e8b-135">Die Form hat eine rote lineare Farbverlaufsfüllung.</span><span class="sxs-lookup"><span data-stu-id="90e8b-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 