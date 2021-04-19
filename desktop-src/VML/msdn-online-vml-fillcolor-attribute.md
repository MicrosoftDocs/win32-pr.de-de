---
title: VML FillColor-Attribut
description: VML FillColor-Attribut
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339093"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="02c53-103">VML FillColor-Attribut</span><span class="sxs-lookup"><span data-stu-id="02c53-103">VML FillColor Attribute</span></span>

<span data-ttu-id="02c53-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="02c53-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="02c53-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="02c53-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="02c53-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="02c53-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="02c53-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="02c53-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="02c53-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="02c53-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="02c53-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="02c53-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="02c53-110">Definiert die Pinsel Farbe, die den geschlossenen Pfad einer Form füllt.</span><span class="sxs-lookup"><span data-stu-id="02c53-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="02c53-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="02c53-111">Read/write.</span></span> <span data-ttu-id="02c53-112">[Ivgcolor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="02c53-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="02c53-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="02c53-113">**Applies To**</span></span>

[<span data-ttu-id="02c53-114">Form</span><span class="sxs-lookup"><span data-stu-id="02c53-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="02c53-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="02c53-115">**Tag Syntax**</span></span>

<span data-ttu-id="02c53-116"><v: *Element* FillColor = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="02c53-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="02c53-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="02c53-117">**Script Syntax**</span></span>

<span data-ttu-id="02c53-118">*Element* . FillColor = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="02c53-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="02c53-119">*Ausdruck* = *Element*. FillColor</span><span class="sxs-lookup"><span data-stu-id="02c53-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="02c53-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="02c53-120">**Remarks**</span></span>

<span data-ttu-id="02c53-121">Der **FillColor** -Wert wird aus dem **Color** -Attribut des **Fill** -Elements dupliziert.</span><span class="sxs-lookup"><span data-stu-id="02c53-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="02c53-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="02c53-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="02c53-123">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="02c53-123">**See Also**</span></span>

<span data-ttu-id="02c53-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [ivgcolor](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="02c53-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="02c53-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="02c53-125">**Example**</span></span>

<span data-ttu-id="02c53-126">Die Füllfarbe des Rechtecks ist rot.</span><span class="sxs-lookup"><span data-stu-id="02c53-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="02c53-127">[FillColor-Attribut Beispiel](/previous-versions/bb229668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="02c53-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="02c53-128">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="02c53-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 