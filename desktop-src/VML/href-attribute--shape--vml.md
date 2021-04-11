---
title: Href-Attribut (Form) (VML)
description: Href-Attribut (Form) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039516"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="512ee-103">Href-Attribut (Form) (VML)</span><span class="sxs-lookup"><span data-stu-id="512ee-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="512ee-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="512ee-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="512ee-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="512ee-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="512ee-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="512ee-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="512ee-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="512ee-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="512ee-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="512ee-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="512ee-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="512ee-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="512ee-110">Definiert eine URL für eine Form.</span><span class="sxs-lookup"><span data-stu-id="512ee-110">Defines a URL for a shape.</span></span> <span data-ttu-id="512ee-111">Beim Klicken auf die Form wird die URL vom Browser geladen.</span><span class="sxs-lookup"><span data-stu-id="512ee-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="512ee-112">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="512ee-112">Read/write.</span></span> <span data-ttu-id="512ee-113">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="512ee-113">**String**.</span></span>

<span data-ttu-id="512ee-114">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="512ee-114">**Applies To**</span></span>

[<span data-ttu-id="512ee-115">Form</span><span class="sxs-lookup"><span data-stu-id="512ee-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="512ee-116">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="512ee-116">**Tag Syntax**</span></span>

<span data-ttu-id="512ee-117"><v: *Element* href = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="512ee-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="512ee-118">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="512ee-118">**Script Syntax**</span></span>

<span data-ttu-id="512ee-119">*Element* . href = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="512ee-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="512ee-120">*Ausdruck* = *Element*. href</span><span class="sxs-lookup"><span data-stu-id="512ee-120">*expression*=*element*.href</span></span>

<span data-ttu-id="512ee-121">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="512ee-121">**Remarks**</span></span>

<span data-ttu-id="512ee-122">Das **href** -Attribut ähnelt dem standardmäßigen HTML- **href** -Attribut von Ankern.</span><span class="sxs-lookup"><span data-stu-id="512ee-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="512ee-123">Die Verwendung von **href** erleichtert das Erstellen interessanter Schaltflächen auf einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="512ee-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="512ee-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="512ee-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="512ee-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="512ee-125">**Example**</span></span>

<span data-ttu-id="512ee-126">Beim Klicken auf das Rechteck lädt der Browser die Microsoft Corporation-Startseite.</span><span class="sxs-lookup"><span data-stu-id="512ee-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="512ee-127">[Href-Attribut Beispiel](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="512ee-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="512ee-128">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="512ee-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 