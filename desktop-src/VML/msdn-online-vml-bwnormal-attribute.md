---
title: VML bwnormal-Attribut
description: VML bwnormal-Attribut
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039198"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="dd90b-103">VML bwnormal-Attribut</span><span class="sxs-lookup"><span data-stu-id="dd90b-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="dd90b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="dd90b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dd90b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="dd90b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dd90b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="dd90b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dd90b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dd90b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dd90b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dd90b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dd90b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dd90b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dd90b-110">Definiert den schwarz-und weiß-Modus für normale schwarze und weiße Ausgabegeräte.</span><span class="sxs-lookup"><span data-stu-id="dd90b-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="dd90b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dd90b-111">Read/write.</span></span> <span data-ttu-id="dd90b-112">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="dd90b-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="dd90b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="dd90b-113">**Applies To**</span></span>

[<span data-ttu-id="dd90b-114">Form</span><span class="sxs-lookup"><span data-stu-id="dd90b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="dd90b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="dd90b-115">**Tag Syntax**</span></span>

<span data-ttu-id="dd90b-116"><v: *Element* o:bwnormal = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="dd90b-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="dd90b-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="dd90b-117">**Remarks**</span></span>

<span data-ttu-id="dd90b-118">Wenn [bwmode](msdn-online-vml-bwmode-attribute.md) auf **Auto** festgelegt ist, wird dieses Attribut verwendet, um zu bestimmen, wie die Form in normalem schwarz und weiß dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd90b-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="dd90b-119">Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="dd90b-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="dd90b-120">Der Standardwert ist " **Auto**".</span><span class="sxs-lookup"><span data-stu-id="dd90b-120">The default value is **auto**.</span></span>

<span data-ttu-id="dd90b-121">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="dd90b-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="dd90b-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="dd90b-122">**Example**</span></span>

<span data-ttu-id="dd90b-123">Die Form wird als Graustufenbild für die normale schwarze und weiße Ausgabe verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dd90b-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 