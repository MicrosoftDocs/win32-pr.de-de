---
description: Das Element der obersten Ebene in einer Journal Notiz-XML-Datei.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Journaldocument-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530170"
---
# <a name="journaldocument-element"></a><span data-ttu-id="0174e-103">Journaldocument-Element</span><span class="sxs-lookup"><span data-stu-id="0174e-103">JournalDocument Element</span></span>

<span data-ttu-id="0174e-104">Das Element der obersten Ebene in einer Journal Notiz-XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="0174e-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="0174e-105">Definition</span><span class="sxs-lookup"><span data-stu-id="0174e-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="0174e-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0174e-106">Parent Elements</span></span>

<span data-ttu-id="0174e-107">Keine</span><span class="sxs-lookup"><span data-stu-id="0174e-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0174e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0174e-108">Child Elements</span></span>

[<span data-ttu-id="0174e-109">**Schreib**</span><span class="sxs-lookup"><span data-stu-id="0174e-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="0174e-110">**Journalpage**</span><span class="sxs-lookup"><span data-stu-id="0174e-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="0174e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="0174e-111">Attributes</span></span>



| <span data-ttu-id="0174e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="0174e-112">Attribute</span></span>             | <span data-ttu-id="0174e-113">type</span><span class="sxs-lookup"><span data-stu-id="0174e-113">Type</span></span>                      | <span data-ttu-id="0174e-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0174e-114">Required</span></span> | <span data-ttu-id="0174e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0174e-115">Description</span></span>                                                      | <span data-ttu-id="0174e-116">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0174e-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0174e-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="0174e-117">**Version**</span></span>           | <span data-ttu-id="0174e-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="0174e-118">**xs:string**</span></span>             | <span data-ttu-id="0174e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0174e-119">Required</span></span> | <span data-ttu-id="0174e-120">Die Version des Journal Dokuments, das in der XML-Datei dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0174e-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="0174e-121">1.0</span><span class="sxs-lookup"><span data-stu-id="0174e-121">1.0</span></span>                       |
| <span data-ttu-id="0174e-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="0174e-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="0174e-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0174e-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0174e-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0174e-124">Required</span></span> | <span data-ttu-id="0174e-125">Die Standardbreite der Seite für das Journal Dokument.</span><span class="sxs-lookup"><span data-stu-id="0174e-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="0174e-126">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0174e-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="0174e-127">**Defaultpageheight**</span><span class="sxs-lookup"><span data-stu-id="0174e-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="0174e-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0174e-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0174e-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0174e-129">Required</span></span> | <span data-ttu-id="0174e-130">Die Standardhöhe der Seite für das Journal Dokument.</span><span class="sxs-lookup"><span data-stu-id="0174e-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="0174e-131">Eine beliebige nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0174e-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0174e-132">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0174e-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="0174e-133">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0174e-133">Element type</span></span> | <span data-ttu-id="0174e-134">**Journaldocument**</span><span class="sxs-lookup"><span data-stu-id="0174e-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="0174e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="0174e-135">Namespace</span></span>    | <span data-ttu-id="0174e-136">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="0174e-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="0174e-137">Schemaname</span><span class="sxs-lookup"><span data-stu-id="0174e-137">Schema name</span></span>  | <span data-ttu-id="0174e-138">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="0174e-138">Journal Reader</span></span>                             |



 

 

 



