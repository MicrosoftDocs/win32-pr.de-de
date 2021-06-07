---
description: Das Element der obersten Ebene in einer XML-Datei mit Journalnotizen.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: JournalDocument-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432172"
---
# <a name="journaldocument-element"></a><span data-ttu-id="33e2c-103">JournalDocument-Element</span><span class="sxs-lookup"><span data-stu-id="33e2c-103">JournalDocument Element</span></span>

<span data-ttu-id="33e2c-104">Das Element der obersten Ebene in einer XML-Datei mit Journalnotizen.</span><span class="sxs-lookup"><span data-stu-id="33e2c-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="33e2c-105">Definition</span><span class="sxs-lookup"><span data-stu-id="33e2c-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="33e2c-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33e2c-106">Parent Elements</span></span>

<span data-ttu-id="33e2c-107">Keine</span><span class="sxs-lookup"><span data-stu-id="33e2c-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="33e2c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33e2c-108">Child Elements</span></span>

[<span data-ttu-id="33e2c-109">**Briefpapier**</span><span class="sxs-lookup"><span data-stu-id="33e2c-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="33e2c-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="33e2c-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="33e2c-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="33e2c-111">Attributes</span></span>



| <span data-ttu-id="33e2c-112">attribute</span><span class="sxs-lookup"><span data-stu-id="33e2c-112">Attribute</span></span>             | <span data-ttu-id="33e2c-113">Typ</span><span class="sxs-lookup"><span data-stu-id="33e2c-113">Type</span></span>                      | <span data-ttu-id="33e2c-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="33e2c-114">Required</span></span> | <span data-ttu-id="33e2c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33e2c-115">Description</span></span>                                                      | <span data-ttu-id="33e2c-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="33e2c-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="33e2c-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="33e2c-117">**Version**</span></span>           | <span data-ttu-id="33e2c-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="33e2c-118">**xs:string**</span></span>             | <span data-ttu-id="33e2c-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="33e2c-119">Required</span></span> | <span data-ttu-id="33e2c-120">Die Version des Journaldokuments, das in der XML-Datei dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33e2c-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="33e2c-121">1.0</span><span class="sxs-lookup"><span data-stu-id="33e2c-121">1.0</span></span>                       |
| <span data-ttu-id="33e2c-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="33e2c-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="33e2c-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="33e2c-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="33e2c-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="33e2c-124">Required</span></span> | <span data-ttu-id="33e2c-125">Die Standardbreite der Seite für das Journaldokument.</span><span class="sxs-lookup"><span data-stu-id="33e2c-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="33e2c-126">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="33e2c-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="33e2c-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="33e2c-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="33e2c-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="33e2c-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="33e2c-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="33e2c-129">Required</span></span> | <span data-ttu-id="33e2c-130">Die Standardhöhe der Seite für das Journaldokument.</span><span class="sxs-lookup"><span data-stu-id="33e2c-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="33e2c-131">Eine nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="33e2c-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="33e2c-132">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="33e2c-132">Element Information</span></span>



|  <span data-ttu-id="33e2c-133">Element</span><span class="sxs-lookup"><span data-stu-id="33e2c-133">Element</span></span>     | <span data-ttu-id="33e2c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="33e2c-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="33e2c-135">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="33e2c-135">Element type</span></span> | <span data-ttu-id="33e2c-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="33e2c-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="33e2c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="33e2c-137">Namespace</span></span>    | <span data-ttu-id="33e2c-138">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="33e2c-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="33e2c-139">Schemaname</span><span class="sxs-lookup"><span data-stu-id="33e2c-139">Schema name</span></span>  | <span data-ttu-id="33e2c-140">Journalreader</span><span class="sxs-lookup"><span data-stu-id="33e2c-140">Journal Reader</span></span>                             |



 

 

 



