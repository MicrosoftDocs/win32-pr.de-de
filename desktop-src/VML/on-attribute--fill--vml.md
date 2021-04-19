---
title: On-Attribut (Fill) (VML)
description: On-Attribut (Fill) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339512"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="356ef-103">On-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="356ef-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="356ef-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="356ef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="356ef-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="356ef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="356ef-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="356ef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="356ef-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="356ef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="356ef-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="356ef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="356ef-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="356ef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="356ef-110">Bestimmt, ob die Füllung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="356ef-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="356ef-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="356ef-111">Read/write.</span></span> <span data-ttu-id="356ef-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="356ef-112">**VgTriState**.</span></span>

<span data-ttu-id="356ef-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="356ef-113">**Applies To**</span></span>

[<span data-ttu-id="356ef-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="356ef-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="356ef-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="356ef-115">**Tag Syntax**</span></span>

<span data-ttu-id="356ef-116"><v: *Element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="356ef-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="356ef-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="356ef-117">**Script Syntax**</span></span>

<span data-ttu-id="356ef-118">*Element* . on = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="356ef-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="356ef-119">*Ausdruck* = *Element*. on</span><span class="sxs-lookup"><span data-stu-id="356ef-119">*expression*=*element*.on</span></span>

<span data-ttu-id="356ef-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="356ef-120">**Remarks**</span></span>

<span data-ttu-id="356ef-121">Wenn der Wert **false** ist, wird die Füllung nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="356ef-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="356ef-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="356ef-122">The default is **True**.</span></span>

<span data-ttu-id="356ef-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="356ef-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="356ef-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="356ef-124">**Example**</span></span>

<span data-ttu-id="356ef-125">Obwohl die Füllung als rot definiert ist, wird Sie nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="356ef-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 