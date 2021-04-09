---
title: VML-textpathok-Attribut
description: VML-textpathok-Attribut
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858278"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="9414f-103">VML-textpathok-Attribut</span><span class="sxs-lookup"><span data-stu-id="9414f-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="9414f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="9414f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9414f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9414f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9414f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="9414f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9414f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9414f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9414f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9414f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9414f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9414f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9414f-110">Bestimmt, ob ein Textpfad angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9414f-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="9414f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9414f-111">Read/write.</span></span> <span data-ttu-id="9414f-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="9414f-112">**VgTriState**.</span></span>

<span data-ttu-id="9414f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="9414f-113">**Applies To**</span></span>

[<span data-ttu-id="9414f-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="9414f-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="9414f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="9414f-115">**Tag Syntax**</span></span>

<span data-ttu-id="9414f-116"><v: *Element* textpathok = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="9414f-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="9414f-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="9414f-117">**Script Syntax**</span></span>

<span data-ttu-id="9414f-118">- *Element* .</span><span class="sxs-lookup"><span data-stu-id="9414f-118">*element* .</span></span> <span data-ttu-id="9414f-119">textpathok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="9414f-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="9414f-120">*Ausdruck* = - *Element*.</span><span class="sxs-lookup"><span data-stu-id="9414f-120">*expression*=*element*.</span></span> <span data-ttu-id="9414f-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="9414f-121">textpathok</span></span>

<span data-ttu-id="9414f-122">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="9414f-122">**Remarks**</span></span>

<span data-ttu-id="9414f-123">Wenn der Wert **false** ist, kann der Pfad keinen Textpfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="9414f-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="9414f-124">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="9414f-124">The default is **False**.</span></span> <span data-ttu-id="9414f-125">Dieses Attribut muss auf " **true** " festgelegt sein, um Text in einem Pfad anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9414f-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="9414f-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="9414f-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="9414f-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="9414f-127">**Example**</span></span>

<span data-ttu-id="9414f-128">Die Form weist einen Textpfad auf.</span><span class="sxs-lookup"><span data-stu-id="9414f-128">The shape has a text path.</span></span> <span data-ttu-id="9414f-129">Der Text "Hello VML" wird in einer Lächeln förmigen Kurve angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9414f-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 