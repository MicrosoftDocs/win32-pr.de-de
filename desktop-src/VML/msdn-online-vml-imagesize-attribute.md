---
title: VML ImageSize-Attribut
description: VML ImageSize-Attribut
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728088"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="c6b81-103">VML ImageSize-Attribut</span><span class="sxs-lookup"><span data-stu-id="c6b81-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="c6b81-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c6b81-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c6b81-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c6b81-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c6b81-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c6b81-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c6b81-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c6b81-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c6b81-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c6b81-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c6b81-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c6b81-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c6b81-110">Definiert die Größe des Bilds für den Strich.</span><span class="sxs-lookup"><span data-stu-id="c6b81-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="c6b81-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c6b81-111">Read/write.</span></span> <span data-ttu-id="c6b81-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="c6b81-112">**VgVector2D**.</span></span>

<span data-ttu-id="c6b81-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c6b81-113">**Applies To**</span></span>

[<span data-ttu-id="c6b81-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="c6b81-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="c6b81-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c6b81-115">**Tag Syntax**</span></span>

<span data-ttu-id="c6b81-116"><v: *Element* ImageSize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c6b81-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="c6b81-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c6b81-117">**Script Syntax**</span></span>

<span data-ttu-id="c6b81-118">*Element* . ImageSize = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c6b81-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="c6b81-119">*Ausdruck* = *Element*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="c6b81-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="c6b81-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c6b81-120">**Remarks**</span></span>

<span data-ttu-id="c6b81-121">Der Standardwert ist die Größe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="c6b81-121">Default is the size of the image.</span></span>

<span data-ttu-id="c6b81-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c6b81-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="c6b81-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c6b81-123">**Example**</span></span>

<span data-ttu-id="c6b81-124">Das Strich Bild ist eine 10-bis-10-Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="c6b81-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 