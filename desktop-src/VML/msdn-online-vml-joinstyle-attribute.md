---
title: VML JOINSTYLE-Attribut
description: VML JOINSTYLE-Attribut
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338670"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="79555-103">VML JOINSTYLE-Attribut</span><span class="sxs-lookup"><span data-stu-id="79555-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="79555-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="79555-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="79555-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="79555-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="79555-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="79555-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="79555-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="79555-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="79555-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="79555-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="79555-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="79555-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="79555-110">Definiert die joinart einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="79555-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="79555-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="79555-111">Read/write.</span></span> <span data-ttu-id="79555-112">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="79555-112">String.</span></span>

<span data-ttu-id="79555-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="79555-113">**Applies To**</span></span>

[<span data-ttu-id="79555-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="79555-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="79555-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="79555-115">**Tag Syntax**</span></span>

<span data-ttu-id="79555-116"><v: *Element* JOINSTYLE = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="79555-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="79555-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="79555-117">**Script Syntax**</span></span>

<span data-ttu-id="79555-118">*Element* . JOINSTYLE = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="79555-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="79555-119">*Ausdruck* = *Element*. JOINSTYLE</span><span class="sxs-lookup"><span data-stu-id="79555-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="79555-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="79555-120">**Remarks**</span></span>

<span data-ttu-id="79555-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="79555-121">Values include:</span></span>

-   <span data-ttu-id="79555-122">Round (Standard)</span><span class="sxs-lookup"><span data-stu-id="79555-122">round (default)</span></span>
-   <span data-ttu-id="79555-123">Abschrägung</span><span class="sxs-lookup"><span data-stu-id="79555-123">bevel</span></span>
-   <span data-ttu-id="79555-124">Gehrungs</span><span class="sxs-lookup"><span data-stu-id="79555-124">miter</span></span>

<span data-ttu-id="79555-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="79555-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="79555-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="79555-126">**Example**</span></span>

<span data-ttu-id="79555-127">Die Gelenke auf der Polylinie werden gevelht.</span><span class="sxs-lookup"><span data-stu-id="79555-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 