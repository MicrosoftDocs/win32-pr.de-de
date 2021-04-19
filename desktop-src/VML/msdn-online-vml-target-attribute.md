---
title: VML-Ziel Attribut
description: VML-Ziel Attribut
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339069"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="a700f-103">VML-Ziel Attribut</span><span class="sxs-lookup"><span data-stu-id="a700f-103">VML Target Attribute</span></span>

<span data-ttu-id="a700f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a700f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a700f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a700f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a700f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a700f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a700f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a700f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a700f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a700f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a700f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a700f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a700f-110">Definiert einen Frame oder ein Fenster, in dem eine URL angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a700f-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="a700f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a700f-111">Read/write.</span></span> <span data-ttu-id="a700f-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="a700f-112">**String**.</span></span>

<span data-ttu-id="a700f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a700f-113">**Applies To**</span></span>

[<span data-ttu-id="a700f-114">Form</span><span class="sxs-lookup"><span data-stu-id="a700f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a700f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a700f-115">**Tag Syntax**</span></span>

<span data-ttu-id="a700f-116"><v: *Element* target = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a700f-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="a700f-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a700f-117">**Remarks**</span></span>

<span data-ttu-id="a700f-118">Das **Ziel** Attribut ähnelt dem Standard-HTML- **Ziel** Attribut von Ankern.</span><span class="sxs-lookup"><span data-stu-id="a700f-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="a700f-119">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a700f-119">Values include:</span></span>



| <span data-ttu-id="a700f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a700f-120">Value</span></span>      | <span data-ttu-id="a700f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a700f-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a700f-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="a700f-122">TargetName</span></span> | <span data-ttu-id="a700f-123">Zeichenfolge, die den Namen des Frames oder Fensters enthält, in dem das Dokument geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a700f-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="a700f-124">\_Blitz</span><span class="sxs-lookup"><span data-stu-id="a700f-124">\_blank</span></span>    | <span data-ttu-id="a700f-125">Gibt an, dass das verknüpfte Dokument in ein neues leeres Fenster geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a700f-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="a700f-126">Dieses Fenster hat keinen Namen.</span><span class="sxs-lookup"><span data-stu-id="a700f-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a700f-127">\_Medien</span><span class="sxs-lookup"><span data-stu-id="a700f-127">\_media</span></span>    | <span data-ttu-id="a700f-128">Ab Internet Explorer 6 für Windows XP Service Pack 2 \_ ist das Medien Attribut veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a700f-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="a700f-129">Der erste in Internet Explorer 6 verfügbare Wert gibt an, dass das verknüpfte Dokument in die Medien Leiste geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a700f-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="a700f-130">\_übergeordneten</span><span class="sxs-lookup"><span data-stu-id="a700f-130">\_parent</span></span>   | <span data-ttu-id="a700f-131">Gibt an, dass das verknüpfte Dokument in das direkt übergeordnete Element des Dokuments geladen wird, das den Link enthält.</span><span class="sxs-lookup"><span data-stu-id="a700f-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a700f-132">\_Such</span><span class="sxs-lookup"><span data-stu-id="a700f-132">\_search</span></span>   | <span data-ttu-id="a700f-133">Ab Internet Explorer 7 für Windows XP Service Pack 2: das \_ Search-Attribut ist veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a700f-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="a700f-134">Der erste in Internet Explorer 6 verfügbare Wert gibt an, dass das verknüpfte Dokument in den Suchbereich des Browsers geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a700f-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="a700f-135">\_self</span><span class="sxs-lookup"><span data-stu-id="a700f-135">\_self</span></span>     | <span data-ttu-id="a700f-136">Gibt an, dass das verknüpfte Dokument in das Fenster geladen wird, in dem auf den Link geklickt wurde (das aktive Fenster).</span><span class="sxs-lookup"><span data-stu-id="a700f-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="a700f-137">\_top</span><span class="sxs-lookup"><span data-stu-id="a700f-137">\_top</span></span>      | <span data-ttu-id="a700f-138">Gibt an, dass das verknüpfte Dokument in das oberste Fenster geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a700f-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="a700f-139">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a700f-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="a700f-140">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a700f-140">**Example**</span></span>

<span data-ttu-id="a700f-141">Beim Klicken auf das Rechteck lädt der Browser die Microsoft Corporation-Startseite im selben Fenster.</span><span class="sxs-lookup"><span data-stu-id="a700f-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="a700f-142">[Beispiel für das Ziel Attribut](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a700f-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="a700f-143">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="a700f-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 