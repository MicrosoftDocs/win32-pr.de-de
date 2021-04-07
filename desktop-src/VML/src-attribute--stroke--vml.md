---
title: Src-Attribut (Strich) (VML)
description: Src-Attribut (Strich) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727544"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="e9d0a-103">Src-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="e9d0a-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="e9d0a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e9d0a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e9d0a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e9d0a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e9d0a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e9d0a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e9d0a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e9d0a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e9d0a-110">Definiert das Quell Bild, das für einen Strich Füllvorgang geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="e9d0a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-111">Read/write.</span></span> <span data-ttu-id="e9d0a-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-112">**String**.</span></span>

<span data-ttu-id="e9d0a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e9d0a-113">**Applies To**</span></span>

[<span data-ttu-id="e9d0a-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="e9d0a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e9d0a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e9d0a-115">**Tag Syntax**</span></span>

<span data-ttu-id="e9d0a-116"><v: *Element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e9d0a-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="e9d0a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e9d0a-117">**Script Syntax**</span></span>

<span data-ttu-id="e9d0a-118">*Element* . src = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e9d0a-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="e9d0a-119">*Ausdruck* = *Element*. src</span><span class="sxs-lookup"><span data-stu-id="e9d0a-119">*expression*=*element*.src</span></span>

<span data-ttu-id="e9d0a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e9d0a-120">**Remarks**</span></span>

<span data-ttu-id="e9d0a-121">Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="e9d0a-122">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="e9d0a-123">Wenn dieses Attribut allein angezeigt wird, d. h. kein **href** oder **Title**, wird das Bild verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="e9d0a-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="e9d0a-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e9d0a-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e9d0a-125">**Example**</span></span>

<span data-ttu-id="e9d0a-126">Der Strich wird mit dem Bild erstellt, das von der cylinder.gif Datei angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9d0a-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 