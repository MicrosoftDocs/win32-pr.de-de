---
title: VML-Aufzählungs Attribut
description: VML-Aufzählungs Attribut
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390539"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="af46c-103">VML-Aufzählungs Attribut</span><span class="sxs-lookup"><span data-stu-id="af46c-103">VML Bullet Attribute</span></span>

<span data-ttu-id="af46c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="af46c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af46c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="af46c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af46c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="af46c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af46c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="af46c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af46c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af46c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af46c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af46c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af46c-110">Bestimmt, ob eine Form eine grafische Kugel ist.</span><span class="sxs-lookup"><span data-stu-id="af46c-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="af46c-111">**VGZ"** lesen/schreiben".</span><span class="sxs-lookup"><span data-stu-id="af46c-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="af46c-112">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="af46c-112">**Applies To**</span></span>

[<span data-ttu-id="af46c-113">Form</span><span class="sxs-lookup"><span data-stu-id="af46c-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="af46c-114">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="af46c-114">**Tag Syntax**</span></span>

<span data-ttu-id="af46c-115"><v: *Element* o:Bullet = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="af46c-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="af46c-116">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="af46c-116">**Remarks**</span></span>

<span data-ttu-id="af46c-117">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="af46c-117">The default is **False**.</span></span> <span data-ttu-id="af46c-118">**True** gibt an, dass die Form eine grafische Kugel ist.</span><span class="sxs-lookup"><span data-stu-id="af46c-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="af46c-119">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="af46c-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="af46c-120">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="af46c-120">**Example**</span></span>

<span data-ttu-id="af46c-121">Die Form ist ein Aufzählungs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af46c-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 