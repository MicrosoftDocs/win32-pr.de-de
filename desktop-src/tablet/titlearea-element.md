---
description: Enthält Speicherort- und Begrenzungsinformationen für den Notiztitel, sofern vorhanden.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432192"
---
# <a name="titlearea-element"></a><span data-ttu-id="4cdd9-103">TitleArea-Element</span><span class="sxs-lookup"><span data-stu-id="4cdd9-103">TitleArea Element</span></span>

<span data-ttu-id="4cdd9-104">Enthält Speicherort- und Begrenzungsinformationen für den Notiztitel, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="4cdd9-105">Definition</span><span class="sxs-lookup"><span data-stu-id="4cdd9-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="4cdd9-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4cdd9-106">Parent Elements</span></span>

[<span data-ttu-id="4cdd9-107">**Titel**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="4cdd9-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4cdd9-108">Child Elements</span></span>

<span data-ttu-id="4cdd9-109">Keine</span><span class="sxs-lookup"><span data-stu-id="4cdd9-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="4cdd9-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4cdd9-110">Attributes</span></span>



| <span data-ttu-id="4cdd9-111">attribute</span><span class="sxs-lookup"><span data-stu-id="4cdd9-111">Attribute</span></span>  | <span data-ttu-id="4cdd9-112">Typ</span><span class="sxs-lookup"><span data-stu-id="4cdd9-112">Type</span></span>                      | <span data-ttu-id="4cdd9-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cdd9-113">Required</span></span> | <span data-ttu-id="4cdd9-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cdd9-114">Description</span></span>                                                                             | <span data-ttu-id="4cdd9-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4cdd9-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="4cdd9-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-116">**Left**</span></span>   | <span data-ttu-id="4cdd9-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-117">**xs:integer**</span></span>            | <span data-ttu-id="4cdd9-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cdd9-118">Required</span></span> | <span data-ttu-id="4cdd9-119">Der Abstand vom Ursprung zum äußersten linken Punkt im begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="4cdd9-120">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-120">Any integer.</span></span>              |
| <span data-ttu-id="4cdd9-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-121">**Top**</span></span>    | <span data-ttu-id="4cdd9-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-122">**xs:integer**</span></span>            | <span data-ttu-id="4cdd9-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cdd9-123">Required</span></span> | <span data-ttu-id="4cdd9-124">Der Abstand vom Ursprung zum obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="4cdd9-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-125">Any integer.</span></span>              |
| <span data-ttu-id="4cdd9-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-126">**Width**</span></span>  | <span data-ttu-id="4cdd9-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4cdd9-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cdd9-128">Required</span></span> | <span data-ttu-id="4cdd9-129">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="4cdd9-130">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="4cdd9-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-131">**Height**</span></span> | <span data-ttu-id="4cdd9-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4cdd9-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cdd9-133">Required</span></span> | <span data-ttu-id="4cdd9-134">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="4cdd9-135">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="4cdd9-136">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4cdd9-136">Element Information</span></span>



|   <span data-ttu-id="4cdd9-137">Element</span><span class="sxs-lookup"><span data-stu-id="4cdd9-137">Element</span></span>    | <span data-ttu-id="4cdd9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="4cdd9-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="4cdd9-139">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="4cdd9-139">Element type</span></span> | <span data-ttu-id="4cdd9-140">[**complexType: TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="4cdd9-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="4cdd9-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cdd9-141">Namespace</span></span>    | <span data-ttu-id="4cdd9-142">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="4cdd9-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="4cdd9-143">Schemaname</span><span class="sxs-lookup"><span data-stu-id="4cdd9-143">Schema name</span></span>  | <span data-ttu-id="4cdd9-144">Journalreader</span><span class="sxs-lookup"><span data-stu-id="4cdd9-144">Journal Reader</span></span>                                                  |



 

 

 



