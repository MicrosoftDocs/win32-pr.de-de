---
title: VML-Format Attribut
description: VML-Format Attribut
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473205"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="e294f-103">VML-Format Attribut</span><span class="sxs-lookup"><span data-stu-id="e294f-103">VML Style Attribute</span></span>

<span data-ttu-id="e294f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e294f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e294f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e294f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e294f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e294f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e294f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e294f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e294f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e294f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e294f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e294f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e294f-110">Definiert den Stil des Frames.</span><span class="sxs-lookup"><span data-stu-id="e294f-110">Defines the style of the frame.</span></span> <span data-ttu-id="e294f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e294f-111">Read/write.</span></span> <span data-ttu-id="e294f-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e294f-112">**String**.</span></span>

<span data-ttu-id="e294f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e294f-113">**Applies To**</span></span>

[<span data-ttu-id="e294f-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="e294f-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="e294f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e294f-115">**Tag Syntax**</span></span>

<span data-ttu-id="e294f-116"><v: *Element* Style = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e294f-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="e294f-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e294f-117">**Script Syntax**</span></span>

<span data-ttu-id="e294f-118">*Element* . Style = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e294f-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="e294f-119">*Ausdruck* = *Element*. Style</span><span class="sxs-lookup"><span data-stu-id="e294f-119">*expression*=*element*.style</span></span>

<span data-ttu-id="e294f-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e294f-120">**Remarks**</span></span>

<span data-ttu-id="e294f-121">Dieses Attribut verwendet die normalen CSS-Stil Attribute für die Positionierung.</span><span class="sxs-lookup"><span data-stu-id="e294f-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="e294f-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="e294f-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="e294f-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e294f-123">**Example**</span></span>

<span data-ttu-id="e294f-124">Der Stil definiert die tatsächliche Position des Frames.</span><span class="sxs-lookup"><span data-stu-id="e294f-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 