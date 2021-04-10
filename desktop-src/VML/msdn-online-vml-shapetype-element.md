---
title: VML ShapeType-Element
description: VML ShapeType-Element
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209254"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="ab582-103">VML ShapeType-Element</span><span class="sxs-lookup"><span data-stu-id="ab582-103">VML ShapeType Element</span></span>

<span data-ttu-id="ab582-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ab582-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ab582-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ab582-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ab582-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ab582-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ab582-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ab582-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ab582-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ab582-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ab582-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ab582-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ab582-110">Definiert eine Form, die zum Erstellen anderer Formen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab582-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="ab582-111">Das folgende Attribut ändert einen **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="ab582-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="ab582-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ab582-112">Attribute</span></span>                                      | <span data-ttu-id="ab582-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab582-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="ab582-114">Master</span><span class="sxs-lookup"><span data-stu-id="ab582-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="ab582-115">Bestimmt, ob ein **ShapeType** ein Master Element ist.</span><span class="sxs-lookup"><span data-stu-id="ab582-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="ab582-116">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ab582-116">**Remarks**</span></span>

<span data-ttu-id="ab582-117">**ShapeType** ist mit dem **Shape** -Element identisch, außer es kann nicht auf ein anderes **ShapeType** -Element verweisen.</span><span class="sxs-lookup"><span data-stu-id="ab582-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="ab582-118">Wenn ein **Shape** -Element auf einen **ShapeType** verweist, kann die **Form** einige der Eigenschaften duplizieren, die bereits im **ShapeType** angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ab582-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="ab582-119">In diesen Fällen überschreiben die Attribute in der **Form** die Attribute des **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="ab582-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="ab582-120">Das **Type** -Attribut darf nicht mit **ShapeType** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab582-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="ab582-121">CSS-Positionierungs Attribute (z. b. " **Top**", " **left**" usw.) werden nicht aus einem **ShapeType** an eine **Form** weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="ab582-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="ab582-122">Um dieses Element zu verwenden, erstellen Sie einen **ShapeType** mit einem bestimmten [ID](id-attribute--vml.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="ab582-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="ab582-123">Erstellen Sie dann eine **Form** , und verweisen Sie auf den **ShapeType** mit dem **Type** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="ab582-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="ab582-124">Weitere Informationen finden Sie unter dem [Type](type-attribute--shape--vml.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="ab582-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 