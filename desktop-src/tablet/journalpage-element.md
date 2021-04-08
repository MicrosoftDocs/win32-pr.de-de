---
description: Enthält die Details zu einer einzelnen Seite in einer Journal Notiz.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Journalpage-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866775"
---
# <a name="journalpage-element"></a><span data-ttu-id="fbc04-103">Journalpage-Element</span><span class="sxs-lookup"><span data-stu-id="fbc04-103">JournalPage Element</span></span>

<span data-ttu-id="fbc04-104">Enthält die Details zu einer einzelnen Seite in einer Journal Notiz.</span><span class="sxs-lookup"><span data-stu-id="fbc04-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="fbc04-105">Definition</span><span class="sxs-lookup"><span data-stu-id="fbc04-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="fbc04-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc04-106">Parent Elements</span></span>

[<span data-ttu-id="fbc04-107">**Journaldocument**</span><span class="sxs-lookup"><span data-stu-id="fbc04-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="fbc04-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc04-108">Child Elements</span></span>

[<span data-ttu-id="fbc04-109">**Stationär**</span><span class="sxs-lookup"><span data-stu-id="fbc04-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="fbc04-110">**Docimage**</span><span class="sxs-lookup"><span data-stu-id="fbc04-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="fbc04-111">**Titleinfo**</span><span class="sxs-lookup"><span data-stu-id="fbc04-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="fbc04-112">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="fbc04-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="fbc04-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbc04-113">Attributes</span></span>



| <span data-ttu-id="fbc04-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="fbc04-114">Attribute</span></span>      | <span data-ttu-id="fbc04-115">type</span><span class="sxs-lookup"><span data-stu-id="fbc04-115">Type</span></span>                      | <span data-ttu-id="fbc04-116">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc04-116">Required</span></span> | <span data-ttu-id="fbc04-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbc04-117">Description</span></span>                                                                        | <span data-ttu-id="fbc04-118">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fbc04-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="fbc04-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="fbc04-119">**Number**</span></span>     | <span data-ttu-id="fbc04-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbc04-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbc04-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc04-121">Required</span></span> | <span data-ttu-id="fbc04-122">Die Ordinalzahl der Seite im Journal Dokument, beginnend mit eins (1).</span><span class="sxs-lookup"><span data-stu-id="fbc04-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="fbc04-123">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fbc04-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="fbc04-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="fbc04-124">**Width**</span></span>      | <span data-ttu-id="fbc04-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbc04-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbc04-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc04-126">Required</span></span> | <span data-ttu-id="fbc04-127">Die Breite der Seite.</span><span class="sxs-lookup"><span data-stu-id="fbc04-127">The width of the page.</span></span>                                                             | <span data-ttu-id="fbc04-128">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fbc04-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="fbc04-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="fbc04-129">**Height**</span></span>     | <span data-ttu-id="fbc04-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbc04-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbc04-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc04-131">Required</span></span> | <span data-ttu-id="fbc04-132">Die Höhe der Seite.</span><span class="sxs-lookup"><span data-stu-id="fbc04-132">The height of the page.</span></span>                                                            | <span data-ttu-id="fbc04-133">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fbc04-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="fbc04-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="fbc04-134">**LineHeight**</span></span> | <span data-ttu-id="fbc04-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbc04-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbc04-136">Optional</span><span class="sxs-lookup"><span data-stu-id="fbc04-136">Optional</span></span> | <span data-ttu-id="fbc04-137">Die Höhe der auf der Seite verwendeten Zeile.</span><span class="sxs-lookup"><span data-stu-id="fbc04-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="fbc04-138">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fbc04-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="fbc04-139">**LanguageID**</span><span class="sxs-lookup"><span data-stu-id="fbc04-139">**LanguageId**</span></span> | <span data-ttu-id="fbc04-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbc04-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbc04-141">Optional</span><span class="sxs-lookup"><span data-stu-id="fbc04-141">Optional</span></span> | <span data-ttu-id="fbc04-142">Die Sprach-ID, die für die Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbc04-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="fbc04-143">Eine nicht negative ganze Zahl, die eine gültige Sprach-ID darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbc04-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="fbc04-144">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fbc04-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="fbc04-145">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="fbc04-145">Element type</span></span> | <span data-ttu-id="fbc04-146">ComplexType für [**journalpagetype**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="fbc04-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="fbc04-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbc04-147">Namespace</span></span>    | <span data-ttu-id="fbc04-148">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="fbc04-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="fbc04-149">Schemaname</span><span class="sxs-lookup"><span data-stu-id="fbc04-149">Schema name</span></span>  | <span data-ttu-id="fbc04-150">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="fbc04-150">Journal Reader</span></span>                                                      |



 

 

 



