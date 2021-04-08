---
title: VML-wrapcoords-Attribut
description: VML-wrapcoords-Attribut
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727961"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="59fd1-103">VML-wrapcoords-Attribut</span><span class="sxs-lookup"><span data-stu-id="59fd1-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="59fd1-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="59fd1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="59fd1-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="59fd1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="59fd1-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="59fd1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="59fd1-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="59fd1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="59fd1-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="59fd1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="59fd1-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="59fd1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="59fd1-110">Definiert das Begrenzungs Polygon, das eine Form umgibt.</span><span class="sxs-lookup"><span data-stu-id="59fd1-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="59fd1-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="59fd1-111">Read/write.</span></span> <span data-ttu-id="59fd1-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="59fd1-112">**String**.</span></span>

<span data-ttu-id="59fd1-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="59fd1-113">**Applies To**</span></span>

[<span data-ttu-id="59fd1-114">Form</span><span class="sxs-lookup"><span data-stu-id="59fd1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="59fd1-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="59fd1-115">**Tag Syntax**</span></span>

<span data-ttu-id="59fd1-116"><v: *Element* o:wrapcoords = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="59fd1-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="59fd1-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="59fd1-117">**Remarks**</span></span>

<span data-ttu-id="59fd1-118">Beschreibt eine durch Trennzeichen getrennte Liste von x und ykoordinaten; Das heißt, "x1, Y1, x2, Y2, X3, Y3,..." Diese wird verwendet, wenn Text eng um eine Form umschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="59fd1-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="59fd1-119">Der Standardwert ist **null** (eine leere Zeichenfolge), bis das **mso-Wrap-Mode-** Attribut auf ' **Tight** ' oder ' **through**' festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="59fd1-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="59fd1-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="59fd1-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="59fd1-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="59fd1-121">**Example**</span></span>

<span data-ttu-id="59fd1-122">Die Form hat ein Begrenzungsfeld mit Text Umbruch, das 5 Einheiten überschreitet, die größer sind als der Pfad.</span><span class="sxs-lookup"><span data-stu-id="59fd1-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 