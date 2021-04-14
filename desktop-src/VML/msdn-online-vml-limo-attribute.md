---
title: VML Limo-Attribut
description: VML Limo-Attribut
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390380"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="44914-103">VML Limo-Attribut</span><span class="sxs-lookup"><span data-stu-id="44914-103">VML Limo Attribute</span></span>

<span data-ttu-id="44914-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="44914-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="44914-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="44914-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="44914-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="44914-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="44914-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="44914-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="44914-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="44914-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="44914-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="44914-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="44914-110">Definiert einen streckungs Punkt auf dem Pfad.</span><span class="sxs-lookup"><span data-stu-id="44914-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="44914-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="44914-111">Read/write.</span></span> <span data-ttu-id="44914-112">**Vector2D**.</span><span class="sxs-lookup"><span data-stu-id="44914-112">**Vector2D**.</span></span>

<span data-ttu-id="44914-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="44914-113">**Applies To**</span></span>

[<span data-ttu-id="44914-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="44914-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="44914-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="44914-115">**Tag Syntax**</span></span>

<span data-ttu-id="44914-116"><v: *Element* Limo = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="44914-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="44914-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="44914-117">**Script Syntax**</span></span>

<span data-ttu-id="44914-118">*Element* . Limo = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="44914-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="44914-119">*Ausdruck* = *Element*. Limo</span><span class="sxs-lookup"><span data-stu-id="44914-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="44914-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="44914-120">**Remarks**</span></span>

<span data-ttu-id="44914-121">Der Standardwert ist "0 0".</span><span class="sxs-lookup"><span data-stu-id="44914-121">The default value is "0 0".</span></span> <span data-ttu-id="44914-122">Limo-Strecken sind Punkte auf dem Edge einer Form, die definieren, wo und wie eine Form von einem Benutzer in einem grafischen Editor gestreckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="44914-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="44914-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="44914-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="44914-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="44914-124">**Example**</span></span>

<span data-ttu-id="44914-125">Ein Limo-streckungs Punkt wird in der Mitte entlang der horizontalen Linie definiert.</span><span class="sxs-lookup"><span data-stu-id="44914-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 