---
title: VML-Attribut "invy"
description: VML-Attribut "invy"
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315536"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="8b81f-103">VML-Attribut "invy"</span><span class="sxs-lookup"><span data-stu-id="8b81f-103">VML InvY Attribute</span></span>

<span data-ttu-id="8b81f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="8b81f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8b81f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="8b81f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8b81f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="8b81f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8b81f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8b81f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8b81f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8b81f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8b81f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8b81f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8b81f-110">Bestimmt, ob die y-Position des Handles invertiert ist.</span><span class="sxs-lookup"><span data-stu-id="8b81f-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="8b81f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8b81f-111">Read/write.</span></span> <span data-ttu-id="8b81f-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="8b81f-112">**VgTriState**.</span></span>

<span data-ttu-id="8b81f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="8b81f-113">**Applies To**</span></span>

<span data-ttu-id="8b81f-114">[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="8b81f-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="8b81f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="8b81f-115">**Tag Syntax**</span></span>

<span data-ttu-id="8b81f-116"><v: *Element* invy = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8b81f-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="8b81f-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8b81f-117">**Remarks**</span></span>

<span data-ttu-id="8b81f-118">**True** gibt an, dass die y-Position des Handles invertiert wird, indem der y-Wert vom y-Wert von **coordorigin** subtrahieren wird, der dem y-Wert von **coordsize** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8b81f-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="8b81f-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="8b81f-119">The default value is **False**.</span></span>

<span data-ttu-id="8b81f-120">Dieses Attribut entspricht</span><span class="sxs-lookup"><span data-stu-id="8b81f-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="8b81f-121">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="8b81f-121">*VML Standard Attribute*</span></span>

 

 