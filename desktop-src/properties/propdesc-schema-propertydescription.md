---
description: Beschreibt eine einzelne eindeutige kanonische Eigenschaft.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertydescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959357"
---
# <a name="propertydescription"></a><span data-ttu-id="eca3f-103">propertydescription</span><span class="sxs-lookup"><span data-stu-id="eca3f-103">propertyDescription</span></span>

<span data-ttu-id="eca3f-104">Beschreibt eine einzelne eindeutige kanonische Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eca3f-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="eca3f-105">Jede solche Eigenschaft, die im System verfügbar sein soll, muss über ein entsprechendes [propertydescription]() -Element verfügen.</span><span class="sxs-lookup"><span data-stu-id="eca3f-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="eca3f-106">Syntax für Windows 7</span><span class="sxs-lookup"><span data-stu-id="eca3f-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="eca3f-107">Syntax für Vista</span><span class="sxs-lookup"><span data-stu-id="eca3f-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="eca3f-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eca3f-108">Element Information</span></span>



| <span data-ttu-id="eca3f-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="eca3f-109">Parent Element</span></span>                                                           | <span data-ttu-id="eca3f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eca3f-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="eca3f-111">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="eca3f-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="eca3f-112">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="eca3f-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="eca3f-113">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="eca3f-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="eca3f-114">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="eca3f-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="eca3f-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="eca3f-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="eca3f-116">Display Info</span><span class="sxs-lookup"><span data-stu-id="eca3f-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="eca3f-117">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="eca3f-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="eca3f-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="eca3f-118">Attributes</span></span>



| <span data-ttu-id="eca3f-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="eca3f-119">Attribute</span></span> | <span data-ttu-id="eca3f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eca3f-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca3f-121">name</span><span class="sxs-lookup"><span data-stu-id="eca3f-121">name</span></span>      | <span data-ttu-id="eca3f-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca3f-122">Required.</span></span> <span data-ttu-id="eca3f-123">Der kanonische Eigenschaftsname, der für das System eindeutig ist. Beispiel: `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="eca3f-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="eca3f-124">Diese Zeichenfolge ist vom Typ "Canonical-Type" und ist auf 64 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="eca3f-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="eca3f-125">Beim Namen wird die Groß-/Kleinschreibung beachtet, und es sollte die folgende Syntax verwendet werden: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="eca3f-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="eca3f-126">[**Ipropertydescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eca3f-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="eca3f-127">FormatID</span><span class="sxs-lookup"><span data-stu-id="eca3f-127">formatID</span></span>  | <span data-ttu-id="eca3f-128">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca3f-128">Required.</span></span> <span data-ttu-id="eca3f-129">Der Format Bezeichner (fmtid) der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eca3f-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="eca3f-130">Der Wert muss einschließende geschweifte Klammern enthalten. Beispiel: `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="eca3f-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="eca3f-131">[**Ipropertydescription:: getpropertykey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eca3f-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="eca3f-132">propID</span><span class="sxs-lookup"><span data-stu-id="eca3f-132">propID</span></span>    | <span data-ttu-id="eca3f-133">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca3f-133">Required.</span></span> <span data-ttu-id="eca3f-134">Der Eigenschaften Bezeichner (PID); Beispiel: `9` .</span><span class="sxs-lookup"><span data-stu-id="eca3f-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="eca3f-135">[**Ipropertydescription:: getpropertykey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eca3f-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="eca3f-136">Dieser Wert muss größer oder gleich 2 sein.</span><span class="sxs-lookup"><span data-stu-id="eca3f-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="eca3f-137">Die Werte 0 und 1 werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="eca3f-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
