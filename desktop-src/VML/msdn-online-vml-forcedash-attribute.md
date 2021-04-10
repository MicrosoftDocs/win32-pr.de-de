---
title: VML forcedash-Attribut
description: VML forcedash-Attribut
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039300"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="69085-103">VML forcedash-Attribut</span><span class="sxs-lookup"><span data-stu-id="69085-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="69085-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="69085-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="69085-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="69085-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="69085-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="69085-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="69085-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="69085-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="69085-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="69085-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="69085-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="69085-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="69085-110">Bestimmt, ob ein gestrichelter Umriss verwendet wird, um eine Form zu zeichnen, wenn eine Form keine Zeile oder Füllung aufweist.</span><span class="sxs-lookup"><span data-stu-id="69085-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="69085-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="69085-111">Read/write.</span></span> <span data-ttu-id="69085-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="69085-112">**VgTriState**.</span></span>

<span data-ttu-id="69085-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="69085-113">**Applies To**</span></span>

[<span data-ttu-id="69085-114">Form</span><span class="sxs-lookup"><span data-stu-id="69085-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="69085-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="69085-115">**Tag Syntax**</span></span>

<span data-ttu-id="69085-116"><v: *Element* o:forcedash = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="69085-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="69085-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="69085-117">**Remarks**</span></span>

<span data-ttu-id="69085-118">Wird von Microsoft PowerPoint-Platzhaltern zum Zeichnen einer gestrichelten Kontur verwendet, wenn keine Zeile und keine Füllung für eine Form vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="69085-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="69085-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="69085-119">Default is **False**.</span></span> <span data-ttu-id="69085-120">Wenn der Wert **true** ist, wird ein gestrichelter Umriss verwendet, um einen Platzhalter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69085-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="69085-121">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="69085-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="69085-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="69085-122">**Example**</span></span>

<span data-ttu-id="69085-123">Eine gestrichelte Linie wird verwendet, um die Form zu Rendering, wenn keine Zeile oder Füllung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="69085-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 