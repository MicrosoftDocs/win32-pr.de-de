---
title: Src-Attribut (imagedata) (VML)
description: Src-Attribut (imagedata) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039053"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="246bb-103">Src-Attribut (imagedata) (VML)</span><span class="sxs-lookup"><span data-stu-id="246bb-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="246bb-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="246bb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="246bb-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="246bb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="246bb-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="246bb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="246bb-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="246bb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="246bb-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="246bb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="246bb-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="246bb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="246bb-110">Definiert eine Quelle für das Bild.</span><span class="sxs-lookup"><span data-stu-id="246bb-110">Defines a source for the image.</span></span> <span data-ttu-id="246bb-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="246bb-111">Read/write.</span></span> <span data-ttu-id="246bb-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="246bb-112">**String**.</span></span>

<span data-ttu-id="246bb-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="246bb-113">**Applies To**</span></span>

[<span data-ttu-id="246bb-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="246bb-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="246bb-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="246bb-115">**Tag Syntax**</span></span>

<span data-ttu-id="246bb-116"><v: *Element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="246bb-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="246bb-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="246bb-117">**Script Syntax**</span></span>

<span data-ttu-id="246bb-118">*Element* . src = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="246bb-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="246bb-119">*Ausdruck* = *Element*. src</span><span class="sxs-lookup"><span data-stu-id="246bb-119">*expression*=*element*.src</span></span>

<span data-ttu-id="246bb-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="246bb-120">**Remarks**</span></span>

<span data-ttu-id="246bb-121">Dieses Attribut muss immer mit dem [imagedata](msdn-online-vml-imagedata-element.md) -Element verwendet werden und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="246bb-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="246bb-122">Wenn dieses Attribut ohne [href](https://www.bing.com/search?q=HRef) oder [Title](title-attribute--imagedata--vml.md)angezeigt wird, wird das Bild verknüpft.</span><span class="sxs-lookup"><span data-stu-id="246bb-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="246bb-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="246bb-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="246bb-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="246bb-124">**Example**</span></span>

<span data-ttu-id="246bb-125">Die Quelle des Bilds ist eine Datei mit dem Namen "kids.jpg".</span><span class="sxs-lookup"><span data-stu-id="246bb-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 