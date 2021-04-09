---
title: VML-Gamma Attribut
description: VML-Gamma Attribut
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101975"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="a6cb8-103">VML-Gamma Attribut</span><span class="sxs-lookup"><span data-stu-id="a6cb8-103">VML Gamma Attribute</span></span>

<span data-ttu-id="a6cb8-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6cb8-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6cb8-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6cb8-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6cb8-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6cb8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6cb8-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6cb8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6cb8-110">Definiert den Kontrast eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="a6cb8-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-111">Read/write.</span></span> <span data-ttu-id="a6cb8-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-112">**VgNumber**.</span></span>

<span data-ttu-id="a6cb8-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a6cb8-113">**Applies To**</span></span>

[<span data-ttu-id="a6cb8-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a6cb8-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a6cb8-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a6cb8-115">**Tag Syntax**</span></span>

<span data-ttu-id="a6cb8-116"><v: *Element* Gamma = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a6cb8-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="a6cb8-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a6cb8-117">**Script Syntax**</span></span>

<span data-ttu-id="a6cb8-118">*Element* . Gamma = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a6cb8-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="a6cb8-119">*Ausdruck* = *Element*. Gamma</span><span class="sxs-lookup"><span data-stu-id="a6cb8-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="a6cb8-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a6cb8-120">**Remarks**</span></span>

<span data-ttu-id="a6cb8-121">Durch das Verringern des Gamma Werts unter 1 wird ein Bild geändert, um es besser zu gestalten, während Werte größer als 1 den Kontrast verringern.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="a6cb8-122">Die nützlichen Werte liegen zwischen 0,3 und 3.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="a6cb8-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a6cb8-123">The default value is 0.</span></span>

<span data-ttu-id="a6cb8-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a6cb8-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a6cb8-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a6cb8-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 