---
title: Color-Attribut (Fill) (VML)
description: Color-Attribut (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473221"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="3b93a-103">Color-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="3b93a-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="3b93a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3b93a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3b93a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3b93a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3b93a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3b93a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3b93a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3b93a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3b93a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3b93a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3b93a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3b93a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3b93a-110">Definiert die Farbe einer Füllung.</span><span class="sxs-lookup"><span data-stu-id="3b93a-110">Defines the color of a fill.</span></span> <span data-ttu-id="3b93a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3b93a-111">Read/write.</span></span> <span data-ttu-id="3b93a-112">**Vgcolor**.</span><span class="sxs-lookup"><span data-stu-id="3b93a-112">**VgColor**.</span></span>

<span data-ttu-id="3b93a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3b93a-113">**Applies To**</span></span>

[<span data-ttu-id="3b93a-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="3b93a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="3b93a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3b93a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3b93a-116"><v: *Element* Color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3b93a-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="3b93a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3b93a-117">**Script Syntax**</span></span>

<span data-ttu-id="3b93a-118">*Element* . Color = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3b93a-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="3b93a-119">*Ausdruck* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="3b93a-119">*expression*=*element*.color</span></span>

<span data-ttu-id="3b93a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3b93a-120">**Remarks**</span></span>

<span data-ttu-id="3b93a-121">Überschreibt das **FillColor** -Attribut einer Form.</span><span class="sxs-lookup"><span data-stu-id="3b93a-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="3b93a-122">Der Standardwert ist **weiß**.</span><span class="sxs-lookup"><span data-stu-id="3b93a-122">The default value is **White**.</span></span>

<span data-ttu-id="3b93a-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3b93a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3b93a-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3b93a-124">**Example**</span></span>

<span data-ttu-id="3b93a-125">Die Füllfarbe der Form ist grün.</span><span class="sxs-lookup"><span data-stu-id="3b93a-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 