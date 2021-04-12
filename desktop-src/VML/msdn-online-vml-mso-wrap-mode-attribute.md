---
title: VML mso-Wrap-Mode-Attribut
description: VML mso-Wrap-Mode-Attribut
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315597"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="74854-103">VML mso-Wrap-Mode-Attribut</span><span class="sxs-lookup"><span data-stu-id="74854-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="74854-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="74854-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74854-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="74854-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74854-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="74854-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74854-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="74854-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74854-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74854-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74854-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74854-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74854-110">Definiert den Wrapping Modus für Text.</span><span class="sxs-lookup"><span data-stu-id="74854-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="74854-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="74854-111">Read/write.</span></span> <span data-ttu-id="74854-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="74854-112">**String**.</span></span>

<span data-ttu-id="74854-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="74854-113">**Applies To**</span></span>

[<span data-ttu-id="74854-114">Form</span><span class="sxs-lookup"><span data-stu-id="74854-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="74854-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="74854-115">**Tag Syntax**</span></span>

<span data-ttu-id="74854-116"><v: *Element* Style = "mso-Wrap-Mode: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="74854-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="74854-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="74854-117">**Remarks**</span></span>

<span data-ttu-id="74854-118">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="74854-118">Values include:</span></span>



| <span data-ttu-id="74854-119">Wert</span><span class="sxs-lookup"><span data-stu-id="74854-119">Value</span></span>          | <span data-ttu-id="74854-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74854-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="74854-121">square</span><span class="sxs-lookup"><span data-stu-id="74854-121">square</span></span>         | <span data-ttu-id="74854-122">Umschließt Text um Form in einem Quadrat.</span><span class="sxs-lookup"><span data-stu-id="74854-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="74854-123">knapper</span><span class="sxs-lookup"><span data-stu-id="74854-123">tight</span></span>          | <span data-ttu-id="74854-124">Text wird in der Nähe der Form umschließt.</span><span class="sxs-lookup"><span data-stu-id="74854-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="74854-125">oben und unten</span><span class="sxs-lookup"><span data-stu-id="74854-125">top-and-bottom</span></span> | <span data-ttu-id="74854-126">Der Text springt von oben nach unten.</span><span class="sxs-lookup"><span data-stu-id="74854-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="74854-127">bis</span><span class="sxs-lookup"><span data-stu-id="74854-127">through</span></span>        | <span data-ttu-id="74854-128">Text wird durch die Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74854-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="74854-129">none</span><span class="sxs-lookup"><span data-stu-id="74854-129">none</span></span>           | <span data-ttu-id="74854-130">Der Text wird nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="74854-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="74854-131">Wird von Microsoft PowerPoint zum Speichern in HTML verwendet, um anzugeben, ob der Zeilenumbruch innerhalb einer AutoForm ein (**quadratisch**) oder Off (**None**) ist.</span><span class="sxs-lookup"><span data-stu-id="74854-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="74854-132">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="74854-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="74854-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="74854-133">**Example**</span></span>

<span data-ttu-id="74854-134">Der folgende Code gibt an, dass WordWrap innerhalb einer AutoShape in PowerPoint aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="74854-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 