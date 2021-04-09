---
title: VML-Attribut "mso-Wrap-Distance-right"
description: VML-Attribut "mso-Wrap-Distance-right"
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf38fc62812b0ce300e4d18067a0f2497233f2e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858324"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a><span data-ttu-id="69c1c-103">VML-Attribut "mso-Wrap-Distance-right"</span><span class="sxs-lookup"><span data-stu-id="69c1c-103">VML MSO-Wrap-Distance-Right Attribute</span></span>

<span data-ttu-id="69c1c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="69c1c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="69c1c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="69c1c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="69c1c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="69c1c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="69c1c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="69c1c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="69c1c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="69c1c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="69c1c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="69c1c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="69c1c-110">Definiert den Abstand zwischen dem rechten Rand der Form und dem Text, der diese umschließt.</span><span class="sxs-lookup"><span data-stu-id="69c1c-110">Defines the distance from the right side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="69c1c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="69c1c-111">Read/write.</span></span> <span data-ttu-id="69c1c-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="69c1c-112">**String**.</span></span>

<span data-ttu-id="69c1c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="69c1c-113">**Applies To**</span></span>

[<span data-ttu-id="69c1c-114">Form</span><span class="sxs-lookup"><span data-stu-id="69c1c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="69c1c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="69c1c-115">**Tag Syntax**</span></span>

<span data-ttu-id="69c1c-116"><v: *Element* Style = "mso-Wrap-Distance-right: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="69c1c-116"><v: *element* style="mso-wrap-distance-right: *expression* "></span></span>

<span data-ttu-id="69c1c-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="69c1c-117">**Remarks**</span></span>

<span data-ttu-id="69c1c-118">Beachten Sie, dass sich dieses Attribut vom CSS **Margin** -Attribut unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="69c1c-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="69c1c-119">Der **Rand** ändert den Ursprung der Form, sodass er die Randbereiche einschließt, aber der Umbruch Abstand in Microsoft Office ändert nicht den Ursprung der Form.</span><span class="sxs-lookup"><span data-stu-id="69c1c-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="69c1c-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="69c1c-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="69c1c-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="69c1c-121">**Example**</span></span>

<span data-ttu-id="69c1c-122">Die Form hat einen rechten Umbruch Abstand von 10 Punkten.</span><span class="sxs-lookup"><span data-stu-id="69c1c-122">The shape has a right wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 