---
description: Enthält Textinformationen aus der Journalnotiz.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432318"
---
# <a name="text-element"></a><span data-ttu-id="02f3e-103">Text-Element</span><span class="sxs-lookup"><span data-stu-id="02f3e-103">Text Element</span></span>

<span data-ttu-id="02f3e-104">Enthält Textinformationen aus der Journalnotiz.</span><span class="sxs-lookup"><span data-stu-id="02f3e-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="02f3e-105">Definition</span><span class="sxs-lookup"><span data-stu-id="02f3e-105">Definition</span></span>

<span data-ttu-id="02f3e-106">Bei Verwendung mit [**Inhalt:**](content-element--journal-reader.md)</span><span class="sxs-lookup"><span data-stu-id="02f3e-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="02f3e-107">Oder, wenn sie mit [**TitleInfo und**](titleinfo-element.md) [**GroupNode verwendet wird:**](groupnode-element.md)</span><span class="sxs-lookup"><span data-stu-id="02f3e-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="02f3e-108">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02f3e-108">Parent Elements</span></span>

[<span data-ttu-id="02f3e-109">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="02f3e-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="02f3e-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="02f3e-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="02f3e-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="02f3e-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="02f3e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02f3e-112">Child Elements</span></span>

<span data-ttu-id="02f3e-113">Keine</span><span class="sxs-lookup"><span data-stu-id="02f3e-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="02f3e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="02f3e-114">Attributes</span></span>

<span data-ttu-id="02f3e-115">Es gibt keine Attribute, wenn sie mit [**TitleInfo und**](titleinfo-element.md) [**GroupNode verwendet werden.**](groupnode-element.md)</span><span class="sxs-lookup"><span data-stu-id="02f3e-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="02f3e-116">Bei Verwendung mit [**Content**](content-element--journal-reader.md)lauten die Attribute wie folgt.</span><span class="sxs-lookup"><span data-stu-id="02f3e-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="02f3e-117">attribute</span><span class="sxs-lookup"><span data-stu-id="02f3e-117">Attribute</span></span>  | <span data-ttu-id="02f3e-118">Typ</span><span class="sxs-lookup"><span data-stu-id="02f3e-118">Type</span></span>                      | <span data-ttu-id="02f3e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02f3e-119">Required</span></span> | <span data-ttu-id="02f3e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02f3e-120">Description</span></span>                                                                             | <span data-ttu-id="02f3e-121">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="02f3e-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="02f3e-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="02f3e-122">**Left**</span></span>   | <span data-ttu-id="02f3e-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="02f3e-123">**xs:integer**</span></span>            | <span data-ttu-id="02f3e-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02f3e-124">Required</span></span> | <span data-ttu-id="02f3e-125">Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="02f3e-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="02f3e-126">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="02f3e-126">Any integer.</span></span>              |
| <span data-ttu-id="02f3e-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="02f3e-127">**Top**</span></span>    | <span data-ttu-id="02f3e-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="02f3e-128">**xs:integer**</span></span>            | <span data-ttu-id="02f3e-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02f3e-129">Required</span></span> | <span data-ttu-id="02f3e-130">Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.</span><span class="sxs-lookup"><span data-stu-id="02f3e-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="02f3e-131">Eine beliebige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="02f3e-131">Any integer.</span></span>              |
| <span data-ttu-id="02f3e-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="02f3e-132">**Width**</span></span>  | <span data-ttu-id="02f3e-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="02f3e-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="02f3e-134">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02f3e-134">Required</span></span> | <span data-ttu-id="02f3e-135">Die Breite des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="02f3e-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="02f3e-136">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="02f3e-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="02f3e-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="02f3e-137">**Height**</span></span> | <span data-ttu-id="02f3e-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="02f3e-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="02f3e-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="02f3e-139">Required</span></span> | <span data-ttu-id="02f3e-140">Die Höhe des Begrenzungsfelds für das Element.</span><span class="sxs-lookup"><span data-stu-id="02f3e-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="02f3e-141">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="02f3e-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="02f3e-142">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="02f3e-142">Element Information</span></span>



|   <span data-ttu-id="02f3e-143">Element</span><span class="sxs-lookup"><span data-stu-id="02f3e-143">Element</span></span>           |   <span data-ttu-id="02f3e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="02f3e-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f3e-145">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="02f3e-145">Element type</span></span> | <span data-ttu-id="02f3e-146">[**complexType:TextType**](texttype-complex-type.md) (mit dem Content-Element) oder **xs:string** (mit [**GroupNode-**](groupnode-element.md) und [**TitleInfo-Elementen)**](titleinfo-element.md)</span><span class="sxs-lookup"><span data-stu-id="02f3e-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="02f3e-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="02f3e-147">Namespace</span></span>    | <span data-ttu-id="02f3e-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="02f3e-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="02f3e-149">Schemaname</span><span class="sxs-lookup"><span data-stu-id="02f3e-149">Schema name</span></span>  | <span data-ttu-id="02f3e-150">Journalreader</span><span class="sxs-lookup"><span data-stu-id="02f3e-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




