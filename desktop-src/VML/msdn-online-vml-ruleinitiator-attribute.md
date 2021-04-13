---
title: VML-ruleinitiator-Attribut
description: VML-ruleinitiator-Attribut
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316358"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="40fd5-103">VML-ruleinitiator-Attribut</span><span class="sxs-lookup"><span data-stu-id="40fd5-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="40fd5-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="40fd5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="40fd5-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="40fd5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="40fd5-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="40fd5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="40fd5-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="40fd5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="40fd5-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="40fd5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="40fd5-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="40fd5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="40fd5-110">Bestimmt, ob eine Regel-Engine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40fd5-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="40fd5-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="40fd5-111">Read/write.</span></span> <span data-ttu-id="40fd5-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="40fd5-112">**VgTriState**.</span></span>

<span data-ttu-id="40fd5-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="40fd5-113">**Applies To**</span></span>

[<span data-ttu-id="40fd5-114">Form</span><span class="sxs-lookup"><span data-stu-id="40fd5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="40fd5-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="40fd5-115">**Tag Syntax**</span></span>

<span data-ttu-id="40fd5-116"><v: *Element* o:ruleinitiator = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="40fd5-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="40fd5-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="40fd5-117">**Remarks**</span></span>

<span data-ttu-id="40fd5-118">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="40fd5-118">The default value is **False**.</span></span> <span data-ttu-id="40fd5-119">Wenn der Wert **true** ist, wird eine Regel-Engine verwendet.</span><span class="sxs-lookup"><span data-stu-id="40fd5-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="40fd5-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="40fd5-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="40fd5-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="40fd5-121">**Example**</span></span>

<span data-ttu-id="40fd5-122">Die Form wird von einer Regel-Engine verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40fd5-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 