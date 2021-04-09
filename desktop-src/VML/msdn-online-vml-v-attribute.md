---
title: VML V-Attribut
description: VML V-Attribut
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101831"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="5fd88-103">VML V-Attribut</span><span class="sxs-lookup"><span data-stu-id="5fd88-103">VML V Attribute</span></span>

<span data-ttu-id="5fd88-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="5fd88-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5fd88-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="5fd88-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5fd88-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="5fd88-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5fd88-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5fd88-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5fd88-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5fd88-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5fd88-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5fd88-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5fd88-110">Definiert die Befehle, die einen Pfad bilden.</span><span class="sxs-lookup"><span data-stu-id="5fd88-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="5fd88-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5fd88-111">Read/write.</span></span> <span data-ttu-id="5fd88-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="5fd88-112">**String**.</span></span>

<span data-ttu-id="5fd88-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="5fd88-113">**Applies To**</span></span>

[<span data-ttu-id="5fd88-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="5fd88-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="5fd88-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="5fd88-115">**Tag Syntax**</span></span>

<span data-ttu-id="5fd88-116"><v: *Element* v = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="5fd88-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="5fd88-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="5fd88-117">**Script Syntax**</span></span>

<span data-ttu-id="5fd88-118">*Element* . v = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="5fd88-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="5fd88-119">*Ausdruck* = *Element*. v</span><span class="sxs-lookup"><span data-stu-id="5fd88-119">*expression*=*element*.v</span></span>

<span data-ttu-id="5fd88-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="5fd88-120">**Remarks**</span></span>

<span data-ttu-id="5fd88-121">Überschreibt das **path** -Attribut einer Form.</span><span class="sxs-lookup"><span data-stu-id="5fd88-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="5fd88-122">Koordinaten können fest Ziffern, relative Zahlen oder Verweise auf Formeln sein (mit dem Format " @n ", wobei "n" eine Formel Nummer ist, z. b. " @2 " bezieht sich auf die zweite Formel im Formel Array).</span><span class="sxs-lookup"><span data-stu-id="5fd88-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="5fd88-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="5fd88-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5fd88-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="5fd88-124">**Example**</span></span>

<span data-ttu-id="5fd88-125">Ein Rechteck wird mit dem **V** -Attribut erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fd88-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="5fd88-126">Beachten Sie, dass nach dem ersten Satz von durch Trennzeichen getrennten Koordinaten ein Kleinbuchstabe L (**LineTo** -Befehl) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fd88-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 