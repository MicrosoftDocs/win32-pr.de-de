---
title: Althref-Attribut (Fill) (VML)
description: Althref-Attribut (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473445"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="1d311-103">Althref-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="1d311-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="1d311-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1d311-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d311-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1d311-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d311-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="1d311-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d311-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d311-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d311-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1d311-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d311-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d311-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d311-110">Definiert einen alternativen Verweis für ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1d311-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="1d311-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1d311-111">Read/write.</span></span> <span data-ttu-id="1d311-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="1d311-112">**String**.</span></span>

<span data-ttu-id="1d311-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="1d311-113">**Applies To**</span></span>

[<span data-ttu-id="1d311-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="1d311-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1d311-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="1d311-115">**Tag Syntax**</span></span>

<span data-ttu-id="1d311-116"><v: *Element* o:althref = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="1d311-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="1d311-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="1d311-117">**Script Syntax**</span></span>

<span data-ttu-id="1d311-118">*Element* . althref = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="1d311-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="1d311-119">*Ausdruck* = *Element*. althref</span><span class="sxs-lookup"><span data-stu-id="1d311-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="1d311-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="1d311-120">**Remarks**</span></span>

<span data-ttu-id="1d311-121">Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping.</span><span class="sxs-lookup"><span data-stu-id="1d311-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="1d311-122">Beim HTML-Schreibvorgang wird die alternative Darstellung (die ursprünglichen Daten, wenn die Datei aus dem Apple Macintosh stammt) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1d311-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="1d311-123">Beim Lesen von HTML wird **althref** gegenüber **src** bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="1d311-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="1d311-124">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="1d311-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="1d311-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="1d311-125">**Example**</span></span>

<span data-ttu-id="1d311-126">Die Füllung der Form hat eine **althref** , die auf eine Datei mit dem Namen "myimage.gif" zeigt.</span><span class="sxs-lookup"><span data-stu-id="1d311-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 