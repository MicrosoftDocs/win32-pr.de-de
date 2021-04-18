---
title: VML-Schaltflächen Attribut
description: VML-Schaltflächen Attribut
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341310"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="b8988-103">VML-Schaltflächen Attribut</span><span class="sxs-lookup"><span data-stu-id="b8988-103">VML Button Attribute</span></span>

<span data-ttu-id="b8988-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="b8988-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b8988-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8988-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b8988-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="b8988-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b8988-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b8988-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b8988-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b8988-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b8988-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b8988-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b8988-110">Bestimmt, ob eine Form als Schaltfläche verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b8988-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="b8988-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b8988-111">Read/write.</span></span> <span data-ttu-id="b8988-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="b8988-112">**VgTriState**.</span></span>

<span data-ttu-id="b8988-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="b8988-113">**Applies To**</span></span>

[<span data-ttu-id="b8988-114">Form</span><span class="sxs-lookup"><span data-stu-id="b8988-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b8988-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="b8988-115">**Tag Syntax**</span></span>

<span data-ttu-id="b8988-116"><v: *Element* o:Button = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="b8988-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="b8988-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="b8988-117">**Remarks**</span></span>

<span data-ttu-id="b8988-118">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="b8988-118">The default is **False**.</span></span> <span data-ttu-id="b8988-119">**True** gibt an, dass die Form als Schaltfläche verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b8988-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="b8988-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="b8988-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b8988-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="b8988-121">**Example**</span></span>

<span data-ttu-id="b8988-122">Die Form ist eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="b8988-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 