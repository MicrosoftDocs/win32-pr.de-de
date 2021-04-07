---
title: Opacity-Attribut (Fill) (VML)
description: Opacity-Attribut (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730136"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="35230-103">Opacity-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="35230-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="35230-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="35230-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="35230-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="35230-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="35230-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="35230-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="35230-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="35230-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="35230-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="35230-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="35230-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="35230-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="35230-110">Definiert die Transparenz einer Füllung.</span><span class="sxs-lookup"><span data-stu-id="35230-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="35230-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="35230-111">Read/write.</span></span> <span data-ttu-id="35230-112">[Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="35230-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="35230-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="35230-113">**Applies To**</span></span>

[<span data-ttu-id="35230-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="35230-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="35230-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="35230-115">**Tag Syntax**</span></span>

<span data-ttu-id="35230-116"><v: *Element* Deckkraft = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="35230-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="35230-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="35230-117">**Script Syntax**</span></span>

<span data-ttu-id="35230-118">*Element* . Opacity = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="35230-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="35230-119">*Ausdruck* = *Element*. Deckkraft</span><span class="sxs-lookup"><span data-stu-id="35230-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="35230-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="35230-120">**Remarks**</span></span>

<span data-ttu-id="35230-121">Der Standardwert ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="35230-121">The default value is 1.0.</span></span>

<span data-ttu-id="35230-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="35230-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="35230-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="35230-123">**Example**</span></span>

<span data-ttu-id="35230-124">Die Füllung der Form ist 50% transparent.</span><span class="sxs-lookup"><span data-stu-id="35230-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 