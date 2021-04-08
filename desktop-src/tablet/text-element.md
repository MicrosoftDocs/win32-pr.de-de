---
description: Enthält Textinformationen aus der Journal Notiz.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960664"
---
# <a name="text-element"></a><span data-ttu-id="27ae8-103">Text-Element</span><span class="sxs-lookup"><span data-stu-id="27ae8-103">Text Element</span></span>

<span data-ttu-id="27ae8-104">Enthält Textinformationen aus der Journal Notiz.</span><span class="sxs-lookup"><span data-stu-id="27ae8-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="27ae8-105">Definition</span><span class="sxs-lookup"><span data-stu-id="27ae8-105">Definition</span></span>

<span data-ttu-id="27ae8-106">Bei Verwendung mit [**Inhalt**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="27ae8-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="27ae8-107">Oder bei Verwendung mit [**titleinfo**](titleinfo-element.md) und [**groupnode**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="27ae8-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="27ae8-108">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27ae8-108">Parent Elements</span></span>

[<span data-ttu-id="27ae8-109">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="27ae8-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="27ae8-110">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="27ae8-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="27ae8-111">**Titleinfo**</span><span class="sxs-lookup"><span data-stu-id="27ae8-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="27ae8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27ae8-112">Child Elements</span></span>

<span data-ttu-id="27ae8-113">Keine</span><span class="sxs-lookup"><span data-stu-id="27ae8-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="27ae8-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="27ae8-114">Attributes</span></span>

<span data-ttu-id="27ae8-115">Es gibt keine Attribute, wenn Sie mit [**titleinfo**](titleinfo-element.md) und [**groupnode**](groupnode-element.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27ae8-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="27ae8-116">Bei Verwendung mit [**Inhalt**](content-element--journal-reader.md)lauten die Attribute wie folgt.</span><span class="sxs-lookup"><span data-stu-id="27ae8-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="27ae8-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="27ae8-117">Attribute</span></span>  | <span data-ttu-id="27ae8-118">type</span><span class="sxs-lookup"><span data-stu-id="27ae8-118">Type</span></span>                      | <span data-ttu-id="27ae8-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27ae8-119">Required</span></span> | <span data-ttu-id="27ae8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27ae8-120">Description</span></span>                                                                             | <span data-ttu-id="27ae8-121">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="27ae8-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="27ae8-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="27ae8-122">**Left**</span></span>   | <span data-ttu-id="27ae8-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="27ae8-123">**xs:integer**</span></span>            | <span data-ttu-id="27ae8-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27ae8-124">Required</span></span> | <span data-ttu-id="27ae8-125">Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements.</span><span class="sxs-lookup"><span data-stu-id="27ae8-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="27ae8-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="27ae8-126">Any integer.</span></span>              |
| <span data-ttu-id="27ae8-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="27ae8-127">**Top**</span></span>    | <span data-ttu-id="27ae8-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="27ae8-128">**xs:integer**</span></span>            | <span data-ttu-id="27ae8-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27ae8-129">Required</span></span> | <span data-ttu-id="27ae8-130">Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.</span><span class="sxs-lookup"><span data-stu-id="27ae8-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="27ae8-131">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="27ae8-131">Any integer.</span></span>              |
| <span data-ttu-id="27ae8-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="27ae8-132">**Width**</span></span>  | <span data-ttu-id="27ae8-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="27ae8-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="27ae8-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27ae8-134">Required</span></span> | <span data-ttu-id="27ae8-135">Die Breite des Begrenzungs Rahmens für das Element.</span><span class="sxs-lookup"><span data-stu-id="27ae8-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="27ae8-136">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="27ae8-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="27ae8-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="27ae8-137">**Height**</span></span> | <span data-ttu-id="27ae8-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="27ae8-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="27ae8-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27ae8-139">Required</span></span> | <span data-ttu-id="27ae8-140">Die Höhe des umgebenden Felds für das Element.</span><span class="sxs-lookup"><span data-stu-id="27ae8-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="27ae8-141">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="27ae8-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="27ae8-142">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="27ae8-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ae8-143">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="27ae8-143">Element type</span></span> | <span data-ttu-id="27ae8-144">ComplexType-Element von [**TextType**](texttype-complex-type.md) (mit dem Content-Element) oder **xs: String** (mit [**groupnode**](groupnode-element.md) -und [**titleinfo**](titleinfo-element.md) -Elementen)</span><span class="sxs-lookup"><span data-stu-id="27ae8-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="27ae8-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="27ae8-145">Namespace</span></span>    | <span data-ttu-id="27ae8-146">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="27ae8-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="27ae8-147">Schemaname</span><span class="sxs-lookup"><span data-stu-id="27ae8-147">Schema name</span></span>  | <span data-ttu-id="27ae8-148">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="27ae8-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




