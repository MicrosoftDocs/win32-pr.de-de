---
description: Enthält die Details zu einer einzelnen Seite in einer Journalnotiz.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432142"
---
# <a name="journalpage-element"></a><span data-ttu-id="a67c1-103">JournalPage-Element</span><span class="sxs-lookup"><span data-stu-id="a67c1-103">JournalPage Element</span></span>

<span data-ttu-id="a67c1-104">Enthält die Details zu einer einzelnen Seite in einer Journalnotiz.</span><span class="sxs-lookup"><span data-stu-id="a67c1-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="a67c1-105">Definition</span><span class="sxs-lookup"><span data-stu-id="a67c1-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="a67c1-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a67c1-106">Parent Elements</span></span>

[<span data-ttu-id="a67c1-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="a67c1-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="a67c1-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a67c1-108">Child Elements</span></span>

[<span data-ttu-id="a67c1-109">**Stationär**</span><span class="sxs-lookup"><span data-stu-id="a67c1-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="a67c1-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="a67c1-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="a67c1-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="a67c1-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="a67c1-112">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="a67c1-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="a67c1-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="a67c1-113">Attributes</span></span>



| <span data-ttu-id="a67c1-114">attribute</span><span class="sxs-lookup"><span data-stu-id="a67c1-114">Attribute</span></span>      | <span data-ttu-id="a67c1-115">Typ</span><span class="sxs-lookup"><span data-stu-id="a67c1-115">Type</span></span>                      | <span data-ttu-id="a67c1-116">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a67c1-116">Required</span></span> | <span data-ttu-id="a67c1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a67c1-117">Description</span></span>                                                                        | <span data-ttu-id="a67c1-118">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a67c1-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a67c1-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="a67c1-119">**Number**</span></span>     | <span data-ttu-id="a67c1-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a67c1-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a67c1-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a67c1-121">Required</span></span> | <span data-ttu-id="a67c1-122">Die Ordnungszahl der Seite im Journaldokument, beginnend mit 1 (1).</span><span class="sxs-lookup"><span data-stu-id="a67c1-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="a67c1-123">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a67c1-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="a67c1-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="a67c1-124">**Width**</span></span>      | <span data-ttu-id="a67c1-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a67c1-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a67c1-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a67c1-126">Required</span></span> | <span data-ttu-id="a67c1-127">Die Breite der Seite.</span><span class="sxs-lookup"><span data-stu-id="a67c1-127">The width of the page.</span></span>                                                             | <span data-ttu-id="a67c1-128">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a67c1-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="a67c1-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="a67c1-129">**Height**</span></span>     | <span data-ttu-id="a67c1-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a67c1-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a67c1-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a67c1-131">Required</span></span> | <span data-ttu-id="a67c1-132">Die Höhe der Seite.</span><span class="sxs-lookup"><span data-stu-id="a67c1-132">The height of the page.</span></span>                                                            | <span data-ttu-id="a67c1-133">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a67c1-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="a67c1-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="a67c1-134">**LineHeight**</span></span> | <span data-ttu-id="a67c1-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a67c1-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a67c1-136">Optional</span><span class="sxs-lookup"><span data-stu-id="a67c1-136">Optional</span></span> | <span data-ttu-id="a67c1-137">Die Höhe der auf der Seite verwendeten Linie.</span><span class="sxs-lookup"><span data-stu-id="a67c1-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="a67c1-138">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a67c1-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="a67c1-139">**Languageid**</span><span class="sxs-lookup"><span data-stu-id="a67c1-139">**LanguageId**</span></span> | <span data-ttu-id="a67c1-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a67c1-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a67c1-141">Optional</span><span class="sxs-lookup"><span data-stu-id="a67c1-141">Optional</span></span> | <span data-ttu-id="a67c1-142">Die sprach-ID, die für die Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a67c1-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="a67c1-143">Eine nicht negative ganze Zahl, die eine gültige Sprach-ID darstellt.</span><span class="sxs-lookup"><span data-stu-id="a67c1-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a67c1-144">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a67c1-144">Element Information</span></span>



|  <span data-ttu-id="a67c1-145">Element</span><span class="sxs-lookup"><span data-stu-id="a67c1-145">Element</span></span>     | <span data-ttu-id="a67c1-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a67c1-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="a67c1-147">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="a67c1-147">Element type</span></span> | <span data-ttu-id="a67c1-148">[**complexType: JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="a67c1-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a67c1-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="a67c1-149">Namespace</span></span>    | <span data-ttu-id="a67c1-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="a67c1-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="a67c1-151">Schemaname</span><span class="sxs-lookup"><span data-stu-id="a67c1-151">Schema name</span></span>  | <span data-ttu-id="a67c1-152">Journalreader</span><span class="sxs-lookup"><span data-stu-id="a67c1-152">Journal Reader</span></span>                                                      |



 

 

 



