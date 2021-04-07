---
title: Origin-Attribut (vmlframe) (VML)
description: Origin-Attribut (vmlframe) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729992"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="ffab2-103">Origin-Attribut (vmlframe) (VML)</span><span class="sxs-lookup"><span data-stu-id="ffab2-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="ffab2-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ffab2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ffab2-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ffab2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ffab2-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ffab2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ffab2-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ffab2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ffab2-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ffab2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ffab2-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ffab2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ffab2-110">Definiert den Ursprung des Clippingbereichs des Frames.</span><span class="sxs-lookup"><span data-stu-id="ffab2-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="ffab2-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ffab2-111">Read/write.</span></span> <span data-ttu-id="ffab2-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ffab2-112">**VgVector2D**.</span></span>

<span data-ttu-id="ffab2-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ffab2-113">**Applies To**</span></span>

[<span data-ttu-id="ffab2-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="ffab2-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="ffab2-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ffab2-115">**Tag Syntax**</span></span>

<span data-ttu-id="ffab2-116"><v: *Element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ffab2-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="ffab2-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ffab2-117">**Script Syntax**</span></span>

<span data-ttu-id="ffab2-118">*Element* . Origin = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="ffab2-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="ffab2-119">*Ausdruck* = *Element*. Origin</span><span class="sxs-lookup"><span data-stu-id="ffab2-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="ffab2-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ffab2-120">**Remarks**</span></span>

<span data-ttu-id="ffab2-121">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="ffab2-121">The default value is 0,0.</span></span> <span data-ttu-id="ffab2-122">Beachten Sie, dass **Origin** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="ffab2-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="ffab2-123">In diesem Attribut wird der Ursprung als die linke obere Ecke des Frames definiert.</span><span class="sxs-lookup"><span data-stu-id="ffab2-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="ffab2-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="ffab2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ffab2-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ffab2-125">**Example**</span></span>

<span data-ttu-id="ffab2-126">Der Ursprung des Clippingbereichs beträgt 100 PT, 100 PT.</span><span class="sxs-lookup"><span data-stu-id="ffab2-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 