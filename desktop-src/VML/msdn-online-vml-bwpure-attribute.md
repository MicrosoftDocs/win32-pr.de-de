---
title: VML bwpure-Attribut
description: VML bwpure-Attribut
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858330"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="c0e98-103">VML bwpure-Attribut</span><span class="sxs-lookup"><span data-stu-id="c0e98-103">VML BWPure Attribute</span></span>

<span data-ttu-id="c0e98-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c0e98-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c0e98-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c0e98-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c0e98-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c0e98-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c0e98-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c0e98-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c0e98-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c0e98-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c0e98-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c0e98-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c0e98-110">Definiert den schwarz-und weißen Modus für reine schwarze und weiße Ausgabegeräte.</span><span class="sxs-lookup"><span data-stu-id="c0e98-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="c0e98-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c0e98-111">Read/write.</span></span> <span data-ttu-id="c0e98-112">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="c0e98-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="c0e98-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c0e98-113">**Applies To**</span></span>

[<span data-ttu-id="c0e98-114">Form</span><span class="sxs-lookup"><span data-stu-id="c0e98-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c0e98-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c0e98-115">**Tag Syntax**</span></span>

<span data-ttu-id="c0e98-116"><v: *Element* o:bwpure = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="c0e98-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="c0e98-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c0e98-117">**Remarks**</span></span>

<span data-ttu-id="c0e98-118">Wenn [bwmode](msdn-online-vml-bwmode-attribute.md) auf **Auto** festgelegt ist, wird dieses Attribut verwendet, um zu bestimmen, wie die Form in rein schwarz und weiß dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0e98-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="c0e98-119">Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="c0e98-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="c0e98-120">Der Standardwert ist " **Auto**".</span><span class="sxs-lookup"><span data-stu-id="c0e98-120">The default is **auto**.</span></span>

<span data-ttu-id="c0e98-121">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="c0e98-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c0e98-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c0e98-122">**Example**</span></span>

<span data-ttu-id="c0e98-123">Die Form wird als Bild mit hohem Kontrast für reine schwarze und weiße Ausgabe verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c0e98-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 