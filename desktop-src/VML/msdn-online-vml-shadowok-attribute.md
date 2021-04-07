---
title: VML shadowok-Attribut
description: VML shadowok-Attribut
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039023"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="2978e-103">VML shadowok-Attribut</span><span class="sxs-lookup"><span data-stu-id="2978e-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="2978e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2978e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2978e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2978e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2978e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2978e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2978e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2978e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2978e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2978e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2978e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2978e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2978e-110">Bestimmt, ob ein Schatten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2978e-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="2978e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2978e-111">Read/write.</span></span> <span data-ttu-id="2978e-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="2978e-112">**VgTriState**.</span></span>

<span data-ttu-id="2978e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2978e-113">**Applies To**</span></span>

[<span data-ttu-id="2978e-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="2978e-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="2978e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2978e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2978e-116"><v: *Element* shadowok = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="2978e-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="2978e-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="2978e-117">**Script Syntax**</span></span>

<span data-ttu-id="2978e-118">*Element* . shadowok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="2978e-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="2978e-119">*Ausdruck* = *Element*. shadowok</span><span class="sxs-lookup"><span data-stu-id="2978e-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="2978e-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2978e-120">**Remarks**</span></span>

<span data-ttu-id="2978e-121">Wenn der Wert **false** ist, kann der Pfad keinen Schatten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2978e-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="2978e-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="2978e-122">The default is **True**.</span></span> <span data-ttu-id="2978e-123">Dieses Attribut überschreibt alle anderen Schatten Attribute im Parent-oder **Shadow** -Element.</span><span class="sxs-lookup"><span data-stu-id="2978e-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="2978e-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2978e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="2978e-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2978e-125">**Example**</span></span>

<span data-ttu-id="2978e-126">Die Form hat keinen Schatten.</span><span class="sxs-lookup"><span data-stu-id="2978e-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 