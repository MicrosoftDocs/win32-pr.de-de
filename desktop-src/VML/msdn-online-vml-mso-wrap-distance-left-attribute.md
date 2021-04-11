---
title: VML-Attribut "mso-Wrap-Distance-Left"
description: VML-Attribut "mso-Wrap-Distance-Left"
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315429"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="1e2e2-103">VML-Attribut "mso-Wrap-Distance-Left"</span><span class="sxs-lookup"><span data-stu-id="1e2e2-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="1e2e2-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1e2e2-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1e2e2-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1e2e2-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1e2e2-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1e2e2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1e2e2-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1e2e2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1e2e2-110">Definiert den Abstand zwischen der linken Seite der Form und dem Text, der diese umschließt.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="1e2e2-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-111">Read/write.</span></span> <span data-ttu-id="1e2e2-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-112">**String**.</span></span>

<span data-ttu-id="1e2e2-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="1e2e2-113">**Applies To**</span></span>

[<span data-ttu-id="1e2e2-114">Form</span><span class="sxs-lookup"><span data-stu-id="1e2e2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1e2e2-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="1e2e2-115">**Tag Syntax**</span></span>

<span data-ttu-id="1e2e2-116"><v: *Element* Style = "mso-Wrap-Distance-left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1e2e2-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="1e2e2-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="1e2e2-117">**Remarks**</span></span>

<span data-ttu-id="1e2e2-118">Beachten Sie, dass sich dieses Attribut vom CSS **Margin** -Attribut unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="1e2e2-119">Der **Rand** ändert den Ursprung der Form, sodass er die Randbereiche einschließt, aber der Umbruch Abstand in Microsoft Office ändert nicht den Ursprung der Form.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="1e2e2-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="1e2e2-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="1e2e2-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="1e2e2-121">**Example**</span></span>

<span data-ttu-id="1e2e2-122">Die Form hat einen linken Umbruch Abstand von 10 Punkten.</span><span class="sxs-lookup"><span data-stu-id="1e2e2-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 