---
title: VML TableProperties-Attribut
description: VML TableProperties-Attribut
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338664"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="3fb8a-103">VML TableProperties-Attribut</span><span class="sxs-lookup"><span data-stu-id="3fb8a-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="3fb8a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3fb8a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3fb8a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3fb8a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3fb8a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3fb8a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3fb8a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3fb8a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3fb8a-110">Bestimmt Tabellen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-110">Determines table properties.</span></span> <span data-ttu-id="3fb8a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-111">Read/write.</span></span> <span data-ttu-id="3fb8a-112">**Integer**.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-112">**Integer**.</span></span>

<span data-ttu-id="3fb8a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3fb8a-113">**Applies To**</span></span>

[<span data-ttu-id="3fb8a-114">Form</span><span class="sxs-lookup"><span data-stu-id="3fb8a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3fb8a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3fb8a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3fb8a-116"><v: *Element* o:TableProperties = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3fb8a-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="3fb8a-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3fb8a-117">**Remarks**</span></span>

<span data-ttu-id="3fb8a-118">Wird von Microsoft PowerPoint für Native Tabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="3fb8a-119">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-119">Default value is 0.</span></span> <span data-ttu-id="3fb8a-120">Nur die ersten drei Bits dieser Ganzzahl werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="3fb8a-121">Obwohl der Wert in einer Form gespeichert ist, ist das-Attribut nur nützlich, wenn die Tabelle aus Formen besteht, die gruppiert sind. Bits können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="3fb8a-122">Die folgenden Bitwerte sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-122">The following bit values are included.</span></span>



| <span data-ttu-id="3fb8a-123">bit</span><span class="sxs-lookup"><span data-stu-id="3fb8a-123">Bit</span></span> | <span data-ttu-id="3fb8a-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3fb8a-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="3fb8a-125">1</span><span class="sxs-lookup"><span data-stu-id="3fb8a-125">1</span></span>   | <span data-ttu-id="3fb8a-126">Legen Sie fest, wenn die Gruppe von Formen eine Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="3fb8a-127">2</span><span class="sxs-lookup"><span data-stu-id="3fb8a-127">2</span></span>   | <span data-ttu-id="3fb8a-128">Legen Sie fest, wenn die Form ein Platzhalter ist.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="3fb8a-129">3</span><span class="sxs-lookup"><span data-stu-id="3fb8a-129">3</span></span>   | <span data-ttu-id="3fb8a-130">Legen Sie fest, ob der Tabellen Text bidirektional ist.</span><span class="sxs-lookup"><span data-stu-id="3fb8a-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="3fb8a-131">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="3fb8a-131">*Microsoft Office Extensions Attribute*</span></span>

 

 