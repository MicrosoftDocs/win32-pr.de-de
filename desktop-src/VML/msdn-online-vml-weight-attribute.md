---
title: VML-Gewichtungs Attribut
description: VML-Gewichtungs Attribut
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337440"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="db0dc-103">VML-Gewichtungs Attribut</span><span class="sxs-lookup"><span data-stu-id="db0dc-103">VML Weight Attribute</span></span>

<span data-ttu-id="db0dc-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="db0dc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="db0dc-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="db0dc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="db0dc-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="db0dc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="db0dc-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="db0dc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="db0dc-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="db0dc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="db0dc-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="db0dc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="db0dc-110">Definiert die Stärke eines Strichs.</span><span class="sxs-lookup"><span data-stu-id="db0dc-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="db0dc-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="db0dc-111">Read/write.</span></span> <span data-ttu-id="db0dc-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="db0dc-112">**String**.</span></span>

<span data-ttu-id="db0dc-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="db0dc-113">**Applies To**</span></span>

[<span data-ttu-id="db0dc-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="db0dc-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="db0dc-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="db0dc-115">**Tag Syntax**</span></span>

<span data-ttu-id="db0dc-116"><v: *Element* Weight = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="db0dc-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="db0dc-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="db0dc-117">**Script Syntax**</span></span>

<span data-ttu-id="db0dc-118">*Element* . Weight = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="db0dc-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="db0dc-119">*Ausdruck* = *Element*. Weight</span><span class="sxs-lookup"><span data-stu-id="db0dc-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="db0dc-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="db0dc-120">**Remarks**</span></span>

<span data-ttu-id="db0dc-121">Dieses Attribut ist mit dem **strokeweight** -Attribut der **Form** identisch und überschreibt es.</span><span class="sxs-lookup"><span data-stu-id="db0dc-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="db0dc-122">Der Standardwert ist 1 Punkt.</span><span class="sxs-lookup"><span data-stu-id="db0dc-122">The default value is 1 point.</span></span>

<span data-ttu-id="db0dc-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="db0dc-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="db0dc-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="db0dc-124">**Example**</span></span>

<span data-ttu-id="db0dc-125">Der Strich hat eine Stärke von 5 Punkten, nicht von 2 Punkten.</span><span class="sxs-lookup"><span data-stu-id="db0dc-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 