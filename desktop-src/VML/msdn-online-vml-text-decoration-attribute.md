---
title: VML-Text-Decoration Attribut
description: VML-Text-Decoration Attribut
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948810"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="75ccd-103">VML-Text-Decoration Attribut</span><span class="sxs-lookup"><span data-stu-id="75ccd-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="75ccd-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="75ccd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="75ccd-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="75ccd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="75ccd-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="75ccd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="75ccd-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="75ccd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="75ccd-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="75ccd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="75ccd-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="75ccd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="75ccd-110">Definiert den Stil der Text Dekoration.</span><span class="sxs-lookup"><span data-stu-id="75ccd-110">Defines the style of text decoration.</span></span> <span data-ttu-id="75ccd-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="75ccd-111">Read/write.</span></span> <span data-ttu-id="75ccd-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="75ccd-112">**String**.</span></span>

<span data-ttu-id="75ccd-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="75ccd-113">**Applies To**</span></span>

[<span data-ttu-id="75ccd-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="75ccd-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="75ccd-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="75ccd-115">**Tag Syntax**</span></span>

<span data-ttu-id="75ccd-116"><v: *Element* Style = "Text-Decoration: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="75ccd-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="75ccd-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="75ccd-117">**Script Syntax**</span></span>

<span data-ttu-id="75ccd-118">*Element* . Style. TextDecoration = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="75ccd-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="75ccd-119">*Ausdruck* = *Element*. Style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="75ccd-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="75ccd-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="75ccd-120">**Remarks**</span></span>

<span data-ttu-id="75ccd-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="75ccd-121">Values include:</span></span>

-   <span data-ttu-id="75ccd-122">keine (Standard)</span><span class="sxs-lookup"><span data-stu-id="75ccd-122">none (default)</span></span>
-   <span data-ttu-id="75ccd-123">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="75ccd-123">underline</span></span>
-   <span data-ttu-id="75ccd-124">Überstrich</span><span class="sxs-lookup"><span data-stu-id="75ccd-124">overline</span></span>
-   <span data-ttu-id="75ccd-125">zeilenweise</span><span class="sxs-lookup"><span data-stu-id="75ccd-125">line-through</span></span>
-   <span data-ttu-id="75ccd-126">blink</span><span class="sxs-lookup"><span data-stu-id="75ccd-126">blink</span></span>

<span data-ttu-id="75ccd-127">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="75ccd-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="75ccd-128">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="75ccd-128">**Example**</span></span>

<span data-ttu-id="75ccd-129">Der Text wird unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="75ccd-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 