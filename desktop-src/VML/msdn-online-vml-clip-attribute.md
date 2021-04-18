---
title: VML-Clip-Attribut
description: VML-Clip-Attribut
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339891"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="2328e-103">VML-Clip-Attribut</span><span class="sxs-lookup"><span data-stu-id="2328e-103">VML Clip Attribute</span></span>

<span data-ttu-id="2328e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2328e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2328e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2328e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2328e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2328e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2328e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2328e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2328e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2328e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2328e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2328e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2328e-110">Bestimmt, ob das Clipping auf ON festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2328e-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="2328e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2328e-111">Read/write.</span></span> <span data-ttu-id="2328e-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="2328e-112">**VgTriState**.</span></span>

<span data-ttu-id="2328e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2328e-113">**Applies To**</span></span>

[<span data-ttu-id="2328e-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="2328e-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="2328e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2328e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2328e-116"><v: *Element* Clip = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2328e-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="2328e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="2328e-117">**Script Syntax**</span></span>

<span data-ttu-id="2328e-118">*Element* . Clip = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="2328e-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="2328e-119">*Ausdruck* = *Element*. Clip</span><span class="sxs-lookup"><span data-stu-id="2328e-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="2328e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2328e-120">**Remarks**</span></span>

<span data-ttu-id="2328e-121">Wenn **Clip** **false** ist, wird die Form so skaliert, dass Sie dem Frame entspricht.</span><span class="sxs-lookup"><span data-stu-id="2328e-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="2328e-122">**True** gibt an, dass Teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2328e-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="2328e-123">Beachten Sie, dass [Origin](origin-attribute--vmlframe--vml.md) und [size](size-attribute--vmlframe.md) nicht verwendet werden, es sei denn, **Clip** ist **true**.</span><span class="sxs-lookup"><span data-stu-id="2328e-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="2328e-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2328e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="2328e-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2328e-125">**Example**</span></span>

<span data-ttu-id="2328e-126">Das in der externen Datei definierte Bild wird abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="2328e-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 