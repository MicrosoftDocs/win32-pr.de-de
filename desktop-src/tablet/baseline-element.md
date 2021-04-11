---
description: Stellt (x, y)-Informationen für die Start-und Endpunkte der Baseline eines Absatzes im Journal Dokument bereit. Der für diese Werte verwendete Koordinaten Bereich ist HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Baseline-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214380"
---
# <a name="baseline-element"></a><span data-ttu-id="137a6-104">Baseline-Element</span><span class="sxs-lookup"><span data-stu-id="137a6-104">Baseline Element</span></span>

<span data-ttu-id="137a6-105">Stellt (x, y)-Informationen für die Start-und Endpunkte der Baseline eines Absatzes im Journal Dokument bereit.</span><span class="sxs-lookup"><span data-stu-id="137a6-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="137a6-106">Der für diese Werte verwendete Koordinaten Bereich ist **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="137a6-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="137a6-107">Definition</span><span class="sxs-lookup"><span data-stu-id="137a6-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="137a6-108">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="137a6-108">Parent Elements</span></span>

[<span data-ttu-id="137a6-109">**Knotenmetriken**</span><span class="sxs-lookup"><span data-stu-id="137a6-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="137a6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="137a6-110">Child Elements</span></span>

<span data-ttu-id="137a6-111">Keine</span><span class="sxs-lookup"><span data-stu-id="137a6-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="137a6-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="137a6-112">Attributes</span></span>



| <span data-ttu-id="137a6-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="137a6-113">Attribute</span></span>  | <span data-ttu-id="137a6-114">type</span><span class="sxs-lookup"><span data-stu-id="137a6-114">Type</span></span>                      | <span data-ttu-id="137a6-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="137a6-115">Required</span></span> | <span data-ttu-id="137a6-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="137a6-116">Description</span></span>                                                      | <span data-ttu-id="137a6-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="137a6-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="137a6-118">**Startx**</span><span class="sxs-lookup"><span data-stu-id="137a6-118">**StartX**</span></span> | <span data-ttu-id="137a6-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="137a6-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="137a6-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="137a6-120">Required</span></span> | <span data-ttu-id="137a6-121">Der X-Wert für den Punkt, der den Anfang der Baseline markiert.</span><span class="sxs-lookup"><span data-stu-id="137a6-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="137a6-122">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="137a6-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="137a6-123">**Startty**</span><span class="sxs-lookup"><span data-stu-id="137a6-123">**StartY**</span></span> | <span data-ttu-id="137a6-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="137a6-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="137a6-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="137a6-125">Required</span></span> | <span data-ttu-id="137a6-126">Der Y-Wert für den Punkt, der den Anfang der Baseline markiert.</span><span class="sxs-lookup"><span data-stu-id="137a6-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="137a6-127">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="137a6-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="137a6-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="137a6-128">**EndX**</span></span>   | <span data-ttu-id="137a6-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="137a6-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="137a6-130">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="137a6-130">Required</span></span> | <span data-ttu-id="137a6-131">Der X-Wert für den Punkt, der das Ende der Baseline markiert.</span><span class="sxs-lookup"><span data-stu-id="137a6-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="137a6-132">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="137a6-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="137a6-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="137a6-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="137a6-134">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="137a6-134">Element type</span></span> | <span data-ttu-id="137a6-135">ComplexType für [**baselinetype**](baselinetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="137a6-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="137a6-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="137a6-136">Namespace</span></span>    | <span data-ttu-id="137a6-137">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="137a6-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="137a6-138">Schemaname</span><span class="sxs-lookup"><span data-stu-id="137a6-138">Schema name</span></span>  | <span data-ttu-id="137a6-139">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="137a6-139">Journal Reader</span></span>                                                |



 

 

 



