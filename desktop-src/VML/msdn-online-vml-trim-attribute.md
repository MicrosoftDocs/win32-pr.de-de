---
title: VML-Trim-Attribut
description: VML-Trim-Attribut
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858435"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="f6e92-103">VML-Trim-Attribut</span><span class="sxs-lookup"><span data-stu-id="f6e92-103">VML Trim Attribute</span></span>

<span data-ttu-id="f6e92-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="f6e92-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6e92-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e92-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6e92-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="f6e92-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6e92-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f6e92-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6e92-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6e92-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6e92-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6e92-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6e92-110">Bestimmt, ob zusätzlicher Leerraum oberhalb und unterhalb des Texts entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f6e92-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="f6e92-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f6e92-111">Read/write.</span></span> <span data-ttu-id="f6e92-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="f6e92-112">**VgTriState**.</span></span>

<span data-ttu-id="f6e92-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="f6e92-113">**Applies To**</span></span>

[<span data-ttu-id="f6e92-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="f6e92-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="f6e92-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="f6e92-115">**Tag Syntax**</span></span>

<span data-ttu-id="f6e92-116"><v: *Element* Style = "Trim: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f6e92-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="f6e92-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="f6e92-117">**Script Syntax**</span></span>

<span data-ttu-id="f6e92-118">*Element* . Style. Trim = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="f6e92-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="f6e92-119">*Ausdruck* = *Element*. Style. Trim</span><span class="sxs-lookup"><span data-stu-id="f6e92-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="f6e92-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="f6e92-120">**Remarks**</span></span>

<span data-ttu-id="f6e92-121">**True** gibt an, dass der für Vorgänger und Nachfolger reservierte Speicherplatz entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f6e92-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="f6e92-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="f6e92-122">The default value is **False**.</span></span>

<span data-ttu-id="f6e92-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="f6e92-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f6e92-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f6e92-124">**Example**</span></span>

<span data-ttu-id="f6e92-125">Der zusätzliche Bereich oberhalb und niedriger wird gekürzt.</span><span class="sxs-lookup"><span data-stu-id="f6e92-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 