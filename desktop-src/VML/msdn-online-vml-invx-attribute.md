---
title: VML-Attribut "invx"
description: VML-Attribut "invx"
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728073"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="535ae-103">VML-Attribut "invx"</span><span class="sxs-lookup"><span data-stu-id="535ae-103">VML InvX Attribute</span></span>

<span data-ttu-id="535ae-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="535ae-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="535ae-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="535ae-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="535ae-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="535ae-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="535ae-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="535ae-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="535ae-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="535ae-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="535ae-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="535ae-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="535ae-110">Bestimmt, ob die x-Position des Handles invertiert ist.</span><span class="sxs-lookup"><span data-stu-id="535ae-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="535ae-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="535ae-111">Read/write.</span></span> <span data-ttu-id="535ae-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="535ae-112">**VgTriState**.</span></span>

<span data-ttu-id="535ae-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="535ae-113">**Applies To**</span></span>

<span data-ttu-id="535ae-114">[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="535ae-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="535ae-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="535ae-115">**Tag Syntax**</span></span>

<span data-ttu-id="535ae-116"><v: *Element* invx = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="535ae-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="535ae-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="535ae-117">**Remarks**</span></span>

<span data-ttu-id="535ae-118">**True** gibt an, dass die x-Position des Handles invertiert wird, indem der x-Wert vom x-Wert von **coordorigin** subtrahieren wird, der dem x-Wert von **coordsize** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="535ae-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="535ae-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="535ae-119">The default value is **False**.</span></span>

<span data-ttu-id="535ae-120">Dieses Attribut entspricht</span><span class="sxs-lookup"><span data-stu-id="535ae-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="535ae-121">coordorigin. x + coordsize. x-h. Position. x</span><span class="sxs-lookup"><span data-stu-id="535ae-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="535ae-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="535ae-122">*VML Standard Attribute*</span></span>

 

 