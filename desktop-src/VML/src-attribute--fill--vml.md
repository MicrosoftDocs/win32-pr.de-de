---
title: Src-Attribut (Fill) (VML)
description: Src-Attribut (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473197"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="dac88-103">Src-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="dac88-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="dac88-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="dac88-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dac88-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="dac88-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dac88-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="dac88-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dac88-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dac88-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dac88-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dac88-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dac88-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dac88-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dac88-110">Definiert das Bild, das für eine Füllung geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dac88-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="dac88-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dac88-111">Read/write.</span></span> <span data-ttu-id="dac88-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="dac88-112">**String**.</span></span>

<span data-ttu-id="dac88-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="dac88-113">**Applies To**</span></span>

[<span data-ttu-id="dac88-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="dac88-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="dac88-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="dac88-115">**Tag Syntax**</span></span>

<span data-ttu-id="dac88-116"><v: *Element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="dac88-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="dac88-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="dac88-117">**Script Syntax**</span></span>

<span data-ttu-id="dac88-118">*Element* . src = "*Ausdruck \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="dac88-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="dac88-119">*Ausdruck* = *Element*. src</span><span class="sxs-lookup"><span data-stu-id="dac88-119">*expression*=*element*.src</span></span>

<span data-ttu-id="dac88-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="dac88-120">**Remarks**</span></span>

<span data-ttu-id="dac88-121">Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dac88-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="dac88-122">Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dac88-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="dac88-123">Wenn dieses Attribut allein angezeigt wird (d. h. kein **href** -oder **Title** -Attribut), wird das Bild verknüpft.</span><span class="sxs-lookup"><span data-stu-id="dac88-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="dac88-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="dac88-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="dac88-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="dac88-125">**Example**</span></span>

<span data-ttu-id="dac88-126">Ein gekacheltes Bild, das die Datei myimage.gif als Quelle verwendet, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dac88-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 