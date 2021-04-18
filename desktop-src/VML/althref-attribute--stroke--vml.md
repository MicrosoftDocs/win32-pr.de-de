---
title: Althref-Attribut (Strich) (VML)
description: Althref-Attribut (Strich) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339291"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="fb563-103">Althref-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="fb563-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="fb563-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="fb563-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fb563-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="fb563-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fb563-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="fb563-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fb563-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fb563-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fb563-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fb563-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fb563-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fb563-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fb563-110">Gibt einen alternativen Verweis für ein Bild an.</span><span class="sxs-lookup"><span data-stu-id="fb563-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="fb563-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="fb563-111">Read/write.</span></span> <span data-ttu-id="fb563-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="fb563-112">**String**.</span></span>

<span data-ttu-id="fb563-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="fb563-113">**Applies To**</span></span>

[<span data-ttu-id="fb563-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="fb563-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="fb563-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="fb563-115">**Tag Syntax**</span></span>

<span data-ttu-id="fb563-116"><v: *Element* o:althref = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="fb563-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="fb563-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="fb563-117">**Script Syntax**</span></span>

<span data-ttu-id="fb563-118">*Element* . althref = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="fb563-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="fb563-119">*Ausdruck* = *Element*. althref</span><span class="sxs-lookup"><span data-stu-id="fb563-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="fb563-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="fb563-120">**Remarks**</span></span>

<span data-ttu-id="fb563-121">Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping.</span><span class="sxs-lookup"><span data-stu-id="fb563-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="fb563-122">Bei HTML-Schreibzugriff die alternative Darstellung (d. h. die ursprünglichen PICT-Daten, wenn die Datei vom Macintosh stammt) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fb563-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="fb563-123">Beim Lesen von HTML wird **althref** gegenüber **src** bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="fb563-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="fb563-124">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="fb563-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="fb563-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="fb563-125">**Example**</span></span>

<span data-ttu-id="fb563-126">Der Strich der Form hat eine **althref** , die auf eine Datei mit dem Namen "myimage.gif" zeigt.</span><span class="sxs-lookup"><span data-stu-id="fb563-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 