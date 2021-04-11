---
title: VML-Attribut "strokeok"
description: VML-Attribut "strokeok"
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948951"
---
# <a name="vml-strokeok-attribute"></a><span data-ttu-id="ad3a9-103">VML-Attribut "strokeok"</span><span class="sxs-lookup"><span data-stu-id="ad3a9-103">VML StrokeOK Attribute</span></span>

<span data-ttu-id="ad3a9-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad3a9-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad3a9-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad3a9-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad3a9-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad3a9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad3a9-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad3a9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad3a9-110">Bestimmt, ob ein Strich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-110">Determines whether a stroke will be displayed.</span></span> <span data-ttu-id="ad3a9-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-111">Read/write.</span></span> <span data-ttu-id="ad3a9-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-112">**VgTriState**.</span></span>

<span data-ttu-id="ad3a9-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ad3a9-113">**Applies To**</span></span>

[<span data-ttu-id="ad3a9-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="ad3a9-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="ad3a9-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ad3a9-115">**Tag Syntax**</span></span>

<span data-ttu-id="ad3a9-116"><v: *Element* strokeok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ad3a9-116"><v: *element* strokeok=" *expression* "></span></span>

<span data-ttu-id="ad3a9-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ad3a9-117">**Script Syntax**</span></span>

<span data-ttu-id="ad3a9-118">*Element* . strokeok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="ad3a9-118">*element* .strokeok="*expression*"</span></span>

<span data-ttu-id="ad3a9-119">*Ausdruck* = *Element*. strokeok</span><span class="sxs-lookup"><span data-stu-id="ad3a9-119">*expression*=*element*.strokeok</span></span>

<span data-ttu-id="ad3a9-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ad3a9-120">**Remarks**</span></span>

<span data-ttu-id="ad3a9-121">Wenn der Wert **false** ist, kann der Pfad nicht gestreichelt werden.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-121">If **False**, the path cannot be stroked.</span></span> <span data-ttu-id="ad3a9-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-122">The default is **True**.</span></span> <span data-ttu-id="ad3a9-123">Dieses Attribut überschreibt alle anderen Strich Attribute im Parent-oder **Stroke** -Element.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-123">This attribute overrides all other stroke attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="ad3a9-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="ad3a9-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ad3a9-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ad3a9-125">**Example**</span></span>

<span data-ttu-id="ad3a9-126">Der Pfad wird nicht mit Strichen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad3a9-126">The path will not be stroked.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 