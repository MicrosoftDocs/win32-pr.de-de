---
title: VML-Attribut "doubleclicknotify"
description: VML-Attribut "doubleclicknotify"
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315236"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="44e9e-103">VML-Attribut "doubleclicknotify"</span><span class="sxs-lookup"><span data-stu-id="44e9e-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="44e9e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="44e9e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="44e9e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="44e9e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="44e9e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="44e9e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="44e9e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="44e9e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="44e9e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="44e9e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="44e9e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="44e9e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="44e9e-110">Sendet eine Ereignismeldung, wenn auf eine Form Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="44e9e-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="44e9e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="44e9e-111">Read/write.</span></span> <span data-ttu-id="44e9e-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="44e9e-112">**VgTriState**.</span></span>

<span data-ttu-id="44e9e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="44e9e-113">**Applies To**</span></span>

[<span data-ttu-id="44e9e-114">Form</span><span class="sxs-lookup"><span data-stu-id="44e9e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="44e9e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="44e9e-115">**Tag Syntax**</span></span>

<span data-ttu-id="44e9e-116"><v: *Element* o:doubleclicknotify = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="44e9e-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="44e9e-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="44e9e-117">**Remarks**</span></span>

<span data-ttu-id="44e9e-118">Der Standardwert ist **false**, was darauf hinweist, dass das Ereignis nicht ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="44e9e-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="44e9e-119">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="44e9e-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="44e9e-120">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="44e9e-120">**Example**</span></span>

<span data-ttu-id="44e9e-121">Bei einem Doppelklick wird durch die Form ein Doppelklick Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="44e9e-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 