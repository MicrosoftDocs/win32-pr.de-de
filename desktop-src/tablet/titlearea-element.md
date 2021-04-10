---
description: Enthält Speicherort und Begrenzungs Informationen für den Notiz Titel, falls vorhanden.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960763"
---
# <a name="titlearea-element"></a><span data-ttu-id="f125b-103">TitleArea-Element</span><span class="sxs-lookup"><span data-stu-id="f125b-103">TitleArea Element</span></span>

<span data-ttu-id="f125b-104">Enthält Speicherort und Begrenzungs Informationen für den Notiz Titel, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f125b-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="f125b-105">Definition</span><span class="sxs-lookup"><span data-stu-id="f125b-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="f125b-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f125b-106">Parent Elements</span></span>

[<span data-ttu-id="f125b-107">**Titel**</span><span class="sxs-lookup"><span data-stu-id="f125b-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="f125b-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f125b-108">Child Elements</span></span>

<span data-ttu-id="f125b-109">Keine</span><span class="sxs-lookup"><span data-stu-id="f125b-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="f125b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f125b-110">Attributes</span></span>



| <span data-ttu-id="f125b-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="f125b-111">Attribute</span></span>  | <span data-ttu-id="f125b-112">type</span><span class="sxs-lookup"><span data-stu-id="f125b-112">Type</span></span>                      | <span data-ttu-id="f125b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f125b-113">Required</span></span> | <span data-ttu-id="f125b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f125b-114">Description</span></span>                                                                             | <span data-ttu-id="f125b-115">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f125b-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f125b-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="f125b-116">**Left**</span></span>   | <span data-ttu-id="f125b-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f125b-117">**xs:integer**</span></span>            | <span data-ttu-id="f125b-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f125b-118">Required</span></span> | <span data-ttu-id="f125b-119">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="f125b-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="f125b-120">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f125b-120">Any integer.</span></span>              |
| <span data-ttu-id="f125b-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="f125b-121">**Top**</span></span>    | <span data-ttu-id="f125b-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f125b-122">**xs:integer**</span></span>            | <span data-ttu-id="f125b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f125b-123">Required</span></span> | <span data-ttu-id="f125b-124">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="f125b-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="f125b-125">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f125b-125">Any integer.</span></span>              |
| <span data-ttu-id="f125b-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="f125b-126">**Width**</span></span>  | <span data-ttu-id="f125b-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f125b-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f125b-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f125b-128">Required</span></span> | <span data-ttu-id="f125b-129">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="f125b-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="f125b-130">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f125b-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="f125b-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="f125b-131">**Height**</span></span> | <span data-ttu-id="f125b-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f125b-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f125b-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f125b-133">Required</span></span> | <span data-ttu-id="f125b-134">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="f125b-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="f125b-135">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f125b-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f125b-136">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f125b-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="f125b-137">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="f125b-137">Element type</span></span> | <span data-ttu-id="f125b-138">ComplexType für [**titleareatype**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="f125b-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f125b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f125b-139">Namespace</span></span>    | <span data-ttu-id="f125b-140">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="f125b-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="f125b-141">Schemaname</span><span class="sxs-lookup"><span data-stu-id="f125b-141">Schema name</span></span>  | <span data-ttu-id="f125b-142">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="f125b-142">Journal Reader</span></span>                                                  |



 

 

 



