---
title: VML-Attribut mit Anmerkungen
description: VML-Attribut mit Anmerkungen
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316292"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="021de-103">VML-Attribut mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="021de-103">VML OnEd Attribute</span></span>

<span data-ttu-id="021de-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="021de-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="021de-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="021de-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="021de-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="021de-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="021de-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="021de-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="021de-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="021de-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="021de-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="021de-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="021de-110">Bestimmt, ob die zusätzlichen Handles einer Form ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="021de-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="021de-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="021de-111">Read/write.</span></span> <span data-ttu-id="021de-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="021de-112">**VgTriState**.</span></span>

<span data-ttu-id="021de-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="021de-113">**Applies To**</span></span>

[<span data-ttu-id="021de-114">Form</span><span class="sxs-lookup"><span data-stu-id="021de-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="021de-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="021de-115">**Tag Syntax**</span></span>

<span data-ttu-id="021de-116"><v: *Element* ' o:oning = ' *Ausdruck* ' ></span><span class="sxs-lookup"><span data-stu-id="021de-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="021de-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="021de-117">**Remarks**</span></span>

<span data-ttu-id="021de-118">Blendet alle Shape-Handles außer der oberen linken und der unteren rechten Ecke aus. Das heißt, die gleichen Handles, die für ein gerades Liniensegment verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="021de-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="021de-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="021de-119">The default is **False**.</span></span>

<span data-ttu-id="021de-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="021de-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="021de-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="021de-121">**Example**</span></span>

<span data-ttu-id="021de-122">Alle außer den linken oberen und unteren rechten Zieh Punkten der Form werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="021de-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 