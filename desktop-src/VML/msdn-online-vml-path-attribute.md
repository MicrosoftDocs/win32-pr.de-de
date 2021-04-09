---
title: VML-Pfad Attribut
description: VML-Pfad Attribut
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858455"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="3c1ee-103">VML-Pfad Attribut</span><span class="sxs-lookup"><span data-stu-id="3c1ee-103">VML Path Attribute</span></span>

<span data-ttu-id="3c1ee-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c1ee-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c1ee-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c1ee-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c1ee-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3c1ee-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c1ee-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3c1ee-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c1ee-110">Gibt die Zeile an, aus der die Ränder einer Form gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="3c1ee-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-111">Read/write.</span></span> <span data-ttu-id="3c1ee-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-112">**String**.</span></span>

<span data-ttu-id="3c1ee-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3c1ee-113">**Applies To**</span></span>

[<span data-ttu-id="3c1ee-114">Form</span><span class="sxs-lookup"><span data-stu-id="3c1ee-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3c1ee-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3c1ee-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c1ee-116"><v: *Element* Path = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3c1ee-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="3c1ee-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3c1ee-117">**Script Syntax**</span></span>

<span data-ttu-id="3c1ee-118">*Element* . Path = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3c1ee-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="3c1ee-119">*Ausdruck* = *Element*. Path</span><span class="sxs-lookup"><span data-stu-id="3c1ee-119">*expression*=*element*.path</span></span>

<span data-ttu-id="3c1ee-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3c1ee-120">**Remarks**</span></span>

<span data-ttu-id="3c1ee-121">Wenn eine Form das [path](msdn-online-vml-path-element.md) -Element enthält, haben die Pfad Befehle des Path-Elements Vorrang vor dem Shape-Attribut Wert.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="3c1ee-122">Weitere Informationen zu dem für Pfade verwendeten Befehlssatz finden Sie im Thema " **Pfad** Element".</span><span class="sxs-lookup"><span data-stu-id="3c1ee-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="3c1ee-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3c1ee-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3c1ee-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3c1ee-124">**Example**</span></span>

<span data-ttu-id="3c1ee-125">Ein geschlossener quadratischer Pfad wird in der Zeichenfolge des Path-Attributs definiert.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="3c1ee-126">Ein Anfangspunkt wird mit `m` (für den Befehl "  Befehl") bei 1, 1 definiert, und eine Linie wird mit `l` (dem Buchstaben "L", der für den Befehl " **LineTo**" verwendet wird) von der Startposition (1, 1) bis zu den anderen drei Punkten (in der Reihenfolge) gezeichnet: 1.200; 200.200; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="3c1ee-127">Die Zeile wird mit `x` (**Close**) geschlossen und endet mit `e` (**Ende**).</span><span class="sxs-lookup"><span data-stu-id="3c1ee-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="3c1ee-128">Beachten Sie, dass Koordinaten im relativen Koordinaten Bereich angegeben werden und dass die tatsächliche Größe durch **Breite** und **Höhe** bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="3c1ee-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="3c1ee-129">[Beispiel für ein Pfad Attribut](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c1ee-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="3c1ee-130">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="3c1ee-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 