---
title: VML-arrowok-Attribut
description: VML-arrowok-Attribut
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390545"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="4b5fe-103">VML-arrowok-Attribut</span><span class="sxs-lookup"><span data-stu-id="4b5fe-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="4b5fe-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4b5fe-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4b5fe-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4b5fe-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4b5fe-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4b5fe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4b5fe-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4b5fe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4b5fe-110">Bestimmt, ob Pfeilspitzen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="4b5fe-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-111">Read/write.</span></span> <span data-ttu-id="4b5fe-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-112">**VgTriState**.</span></span>

<span data-ttu-id="4b5fe-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="4b5fe-113">**Applies To**</span></span>

[<span data-ttu-id="4b5fe-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="4b5fe-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="4b5fe-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="4b5fe-115">**Tag Syntax**</span></span>

<span data-ttu-id="4b5fe-116"><v: *Element* arrowok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4b5fe-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="4b5fe-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="4b5fe-117">**Script Syntax**</span></span>

<span data-ttu-id="4b5fe-118">*Element* . arrowok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="4b5fe-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="4b5fe-119">*Ausdruck* = *Element*. arrowok</span><span class="sxs-lookup"><span data-stu-id="4b5fe-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="4b5fe-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4b5fe-120">**Remarks**</span></span>

<span data-ttu-id="4b5fe-121">Wenn der Wert **false** ist, weist der Pfad keine Pfeilspitzen auf.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="4b5fe-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-122">The default is **False**.</span></span> <span data-ttu-id="4b5fe-123">Dieses Attribut überschreibt alle anderen Pfeilspitze-Attribute im Parent-oder **Stroke** -Element.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="4b5fe-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="4b5fe-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4b5fe-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="4b5fe-125">**Example**</span></span>

<span data-ttu-id="4b5fe-126">Der Pfad weist keine Pfeilspitze auf.</span><span class="sxs-lookup"><span data-stu-id="4b5fe-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 