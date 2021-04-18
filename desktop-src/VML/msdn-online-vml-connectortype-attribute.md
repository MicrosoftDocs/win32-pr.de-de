---
title: VML Connector Type-Attribut
description: VML Connector Type-Attribut
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340495"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="d43da-103">VML Connector Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="d43da-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="d43da-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d43da-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d43da-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d43da-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d43da-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d43da-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d43da-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d43da-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d43da-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d43da-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d43da-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d43da-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d43da-110">Gibt den Verbindungstyp an, der zum Verbinden von Formen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d43da-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="d43da-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d43da-111">Read/write.</span></span> <span data-ttu-id="d43da-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="d43da-112">**String**.</span></span>

<span data-ttu-id="d43da-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="d43da-113">**Applies To**</span></span>

[<span data-ttu-id="d43da-114">Form</span><span class="sxs-lookup"><span data-stu-id="d43da-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d43da-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="d43da-115">**Tag Syntax**</span></span>

<span data-ttu-id="d43da-116"><v: *Element* o:Connector Type = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d43da-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="d43da-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="d43da-117">**Remarks**</span></span>

<span data-ttu-id="d43da-118">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="d43da-118">Values include:</span></span>



| <span data-ttu-id="d43da-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d43da-119">Value</span></span>    | <span data-ttu-id="d43da-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d43da-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="d43da-121">none</span><span class="sxs-lookup"><span data-stu-id="d43da-121">none</span></span>     | <span data-ttu-id="d43da-122">Kein Connector.</span><span class="sxs-lookup"><span data-stu-id="d43da-122">No connector.</span></span>                  |
| <span data-ttu-id="d43da-123">direkte</span><span class="sxs-lookup"><span data-stu-id="d43da-123">straight</span></span> | <span data-ttu-id="d43da-124">Standard.</span><span class="sxs-lookup"><span data-stu-id="d43da-124">Default.</span></span> <span data-ttu-id="d43da-125">Ein geradliniger Connector.</span><span class="sxs-lookup"><span data-stu-id="d43da-125">A straight connector.</span></span> |
| <span data-ttu-id="d43da-126">Bogens</span><span class="sxs-lookup"><span data-stu-id="d43da-126">elbow</span></span>    | <span data-ttu-id="d43da-127">Ein von einem Elbow geformter Connector.</span><span class="sxs-lookup"><span data-stu-id="d43da-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="d43da-128">MMT</span><span class="sxs-lookup"><span data-stu-id="d43da-128">curved</span></span>   | <span data-ttu-id="d43da-129">Ein gekrümmter Connector.</span><span class="sxs-lookup"><span data-stu-id="d43da-129">A curved connector.</span></span>            |



 

<span data-ttu-id="d43da-130">Dieses Attribut kann auch von einer Regel-Engine eines grafischen Editors verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d43da-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="d43da-131">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="d43da-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="d43da-132">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="d43da-132">**Example**</span></span>

<span data-ttu-id="d43da-133">Die Form verwendet eine gerade Linie als Connector.</span><span class="sxs-lookup"><span data-stu-id="d43da-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 