---
title: On-Attribut (Strich) (VML)
description: On-Attribut (Strich) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337857"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="96cb4-103">On-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="96cb4-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="96cb4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="96cb4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96cb4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="96cb4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96cb4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="96cb4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96cb4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="96cb4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96cb4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="96cb4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96cb4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="96cb4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96cb4-110">Bestimmt, ob der Strich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96cb4-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="96cb4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="96cb4-111">Read/write.</span></span> <span data-ttu-id="96cb4-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="96cb4-112">**VgTriState**.</span></span>

<span data-ttu-id="96cb4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="96cb4-113">**Applies To**</span></span>

[<span data-ttu-id="96cb4-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="96cb4-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="96cb4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="96cb4-115">**Tag Syntax**</span></span>

<span data-ttu-id="96cb4-116"><v: *Element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="96cb4-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="96cb4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="96cb4-117">**Script Syntax**</span></span>

<span data-ttu-id="96cb4-118">*Element* . on = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="96cb4-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="96cb4-119">*Ausdruck* = *Element*. on</span><span class="sxs-lookup"><span data-stu-id="96cb4-119">*expression*=*element*.on</span></span>

<span data-ttu-id="96cb4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="96cb4-120">**Remarks**</span></span>

<span data-ttu-id="96cb4-121">Wenn der Wert **false** ist, wird der Strich nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96cb4-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="96cb4-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="96cb4-122">The default is **True**.</span></span>

<span data-ttu-id="96cb4-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="96cb4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="96cb4-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="96cb4-124">**Example**</span></span>

<span data-ttu-id="96cb4-125">Der Strich wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96cb4-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 